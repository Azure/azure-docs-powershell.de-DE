---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: 751a551f5ed0a0a1968c74e5f94bcabad3b5ff32
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844668"
---
# <span data-ttu-id="d866a-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="d866a-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="d866a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d866a-102">SYNOPSIS</span></span>
<span data-ttu-id="d866a-103">Auflisten aller Compute-Ressourcen-SKUs</span><span class="sxs-lookup"><span data-stu-id="d866a-103">List all compute resource Skus</span></span>

## <span data-ttu-id="d866a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d866a-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d866a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d866a-105">DESCRIPTION</span></span>
<span data-ttu-id="d866a-106">Auflisten aller Compute-Ressourcen-SKUs</span><span class="sxs-lookup"><span data-stu-id="d866a-106">List all compute resource Skus</span></span>

## <span data-ttu-id="d866a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d866a-107">EXAMPLES</span></span>

### <span data-ttu-id="d866a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d866a-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="d866a-109">Auflisten aller Compute-Ressourcen-SKUs in der Region West-US</span><span class="sxs-lookup"><span data-stu-id="d866a-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="d866a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d866a-110">PARAMETERS</span></span>

### <span data-ttu-id="d866a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d866a-111">-DefaultProfile</span></span>
<span data-ttu-id="d866a-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d866a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d866a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d866a-113">CommonParameters</span></span>
<span data-ttu-id="d866a-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d866a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d866a-115">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d866a-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d866a-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d866a-116">INPUTS</span></span>

### <span data-ttu-id="d866a-117">Keine</span><span class="sxs-lookup"><span data-stu-id="d866a-117">None</span></span>

## <span data-ttu-id="d866a-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d866a-118">OUTPUTS</span></span>

### <span data-ttu-id="d866a-119">System. Object</span><span class="sxs-lookup"><span data-stu-id="d866a-119">System.Object</span></span>

## <span data-ttu-id="d866a-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="d866a-120">NOTES</span></span>

## <span data-ttu-id="d866a-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d866a-121">RELATED LINKS</span></span>

