---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: c15a8b57338a6c5e7c2f054e07a0d26d716627fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822375"
---
# <span data-ttu-id="63442-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="63442-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="63442-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="63442-102">SYNOPSIS</span></span>
<span data-ttu-id="63442-103">Ruft eine Azure Express Route-Kreuzverbindung aus Azure ab.</span><span class="sxs-lookup"><span data-stu-id="63442-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="63442-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="63442-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63442-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63442-105">DESCRIPTION</span></span>
<span data-ttu-id="63442-106">Das Cmdlet " **Get-AzExpressRouteCrossConnection** " wird verwendet, um ein Express Route-Kreuz Verbindungsobjekt aus Ihrem Abonnement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="63442-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="63442-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="63442-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="63442-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="63442-108">EXAMPLES</span></span>

### <span data-ttu-id="63442-109">Beispiel 1: Abrufen der Express Route-Querverbindung</span><span class="sxs-lookup"><span data-stu-id="63442-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="63442-110">Beispiel 2: Auflisten der Express Route-Querverbindungen mithilfe eines Filters</span><span class="sxs-lookup"><span data-stu-id="63442-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="63442-111">Mit diesem Cmdlet werden alle Express Route-Querverbindungen aufgelistet, die mit "Test" beginnen.</span><span class="sxs-lookup"><span data-stu-id="63442-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="63442-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="63442-112">PARAMETERS</span></span>

### <span data-ttu-id="63442-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63442-113">-DefaultProfile</span></span>
<span data-ttu-id="63442-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="63442-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63442-115">-Name</span><span class="sxs-lookup"><span data-stu-id="63442-115">-Name</span></span>
<span data-ttu-id="63442-116">Der Name der Express Route-Querverbindung.</span><span class="sxs-lookup"><span data-stu-id="63442-116">The name of the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="63442-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63442-117">-ResourceGroupName</span></span>
<span data-ttu-id="63442-118">Der Name der Ressourcengruppe, die die Express Route-Querverbindung enthält.</span><span class="sxs-lookup"><span data-stu-id="63442-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="63442-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63442-119">CommonParameters</span></span>
<span data-ttu-id="63442-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63442-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63442-121">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63442-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63442-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="63442-122">INPUTS</span></span>

### <span data-ttu-id="63442-123">Keine</span><span class="sxs-lookup"><span data-stu-id="63442-123">None</span></span>
<span data-ttu-id="63442-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="63442-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="63442-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="63442-125">OUTPUTS</span></span>

### <span data-ttu-id="63442-126">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="63442-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="63442-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="63442-127">NOTES</span></span>

## <span data-ttu-id="63442-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="63442-128">RELATED LINKS</span></span>

[<span data-ttu-id="63442-129">Satz-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="63442-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)