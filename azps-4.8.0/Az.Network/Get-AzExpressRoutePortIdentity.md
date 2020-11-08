---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
ms.openlocfilehash: 246675a2473bb20e5040f3898b6931f1b3ee6933
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174362"
---
# <span data-ttu-id="e6c83-101">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="e6c83-101">Get-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="e6c83-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e6c83-102">SYNOPSIS</span></span>
<span data-ttu-id="e6c83-103">Abrufen einer einem ExpressRoutePort zugewiesenen Identität</span><span class="sxs-lookup"><span data-stu-id="e6c83-103">Get identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="e6c83-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6c83-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6c83-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e6c83-105">DESCRIPTION</span></span>
<span data-ttu-id="e6c83-106">Das Cmdlet " **Get-AzExpressRoutePortIdentity** " Ruft eine Identität ab, die einem lokalen Azure ExpressRoutePort-Objekt zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="e6c83-106">The **Get-AzExpressRoutePortIdentity** cmdlet gets identity assigned to a local Azure ExpressRoutePort object.</span></span>

## <span data-ttu-id="e6c83-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e6c83-107">EXAMPLES</span></span>

### <span data-ttu-id="e6c83-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e6c83-108">Example 1</span></span>
```powershell
PS C:\> $exrPort = Get-AzExpressRoutePort -Name $exrPortName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzExpressRoutePortIdentity -ExpressRoutePort $exrPort
```

## <span data-ttu-id="e6c83-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6c83-109">PARAMETERS</span></span>

### <span data-ttu-id="e6c83-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6c83-110">-DefaultProfile</span></span>
<span data-ttu-id="e6c83-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e6c83-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6c83-112">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e6c83-112">-ExpressRoutePort</span></span>
<span data-ttu-id="e6c83-113">Der Express Route-Port</span><span class="sxs-lookup"><span data-stu-id="e6c83-113">The ExpressRoute Port</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6c83-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6c83-114">CommonParameters</span></span>
<span data-ttu-id="e6c83-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6c83-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6c83-116">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6c83-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6c83-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e6c83-117">INPUTS</span></span>

### <span data-ttu-id="e6c83-118">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e6c83-118">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="e6c83-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e6c83-119">OUTPUTS</span></span>

### <span data-ttu-id="e6c83-120">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="e6c83-120">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="e6c83-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="e6c83-121">NOTES</span></span>

## <span data-ttu-id="e6c83-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e6c83-122">RELATED LINKS</span></span>
[<span data-ttu-id="e6c83-123">Satz-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="e6c83-123">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="e6c83-124">Neu – AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="e6c83-124">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="e6c83-125">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="e6c83-125">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)