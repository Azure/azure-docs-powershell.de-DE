---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: ab57e922a7ef63d14a36bbd91ed268822e2c61e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003897"
---
# <span data-ttu-id="9c803-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="9c803-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="9c803-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9c803-102">SYNOPSIS</span></span>
<span data-ttu-id="9c803-103">Auflisten aller Compute-Ressourcen-SKUs</span><span class="sxs-lookup"><span data-stu-id="9c803-103">List all compute resource Skus</span></span>

## <span data-ttu-id="9c803-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c803-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c803-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c803-105">DESCRIPTION</span></span>
<span data-ttu-id="9c803-106">Auflisten aller Compute-Ressourcen-SKUs</span><span class="sxs-lookup"><span data-stu-id="9c803-106">List all compute resource Skus</span></span>

## <span data-ttu-id="9c803-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9c803-107">EXAMPLES</span></span>

### <span data-ttu-id="9c803-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9c803-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="9c803-109">Auflisten aller Compute-Ressourcen-SKUs in der Region West-US</span><span class="sxs-lookup"><span data-stu-id="9c803-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="9c803-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c803-110">PARAMETERS</span></span>

### <span data-ttu-id="9c803-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c803-111">-DefaultProfile</span></span>
<span data-ttu-id="9c803-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9c803-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c803-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c803-113">CommonParameters</span></span>
<span data-ttu-id="9c803-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c803-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c803-115">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c803-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c803-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9c803-116">INPUTS</span></span>

### <span data-ttu-id="9c803-117">Keine</span><span class="sxs-lookup"><span data-stu-id="9c803-117">None</span></span>

## <span data-ttu-id="9c803-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9c803-118">OUTPUTS</span></span>

### <span data-ttu-id="9c803-119">Microsoft. Azure. Commands. Compute. Automation. Models. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="9c803-119">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="9c803-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="9c803-120">NOTES</span></span>

## <span data-ttu-id="9c803-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9c803-121">RELATED LINKS</span></span>
