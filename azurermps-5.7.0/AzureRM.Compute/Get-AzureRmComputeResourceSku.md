---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
ms.openlocfilehash: b9e1c42ca3a67a80a939a4e79626253b903764f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478642"
---
# <span data-ttu-id="36e32-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="36e32-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="36e32-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="36e32-102">SYNOPSIS</span></span>
<span data-ttu-id="36e32-103">Auflisten aller Compute-Ressourcen-SKUs</span><span class="sxs-lookup"><span data-stu-id="36e32-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36e32-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="36e32-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [<CommonParameters>]
```

## <span data-ttu-id="36e32-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36e32-105">DESCRIPTION</span></span>
<span data-ttu-id="36e32-106">Auflisten aller Compute-Ressourcen-SKUs</span><span class="sxs-lookup"><span data-stu-id="36e32-106">List all compute resource Skus</span></span>

## <span data-ttu-id="36e32-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="36e32-107">EXAMPLES</span></span>

### <span data-ttu-id="36e32-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="36e32-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="36e32-109">Auflisten aller Compute-Ressourcen-SKUs in der Region West-US</span><span class="sxs-lookup"><span data-stu-id="36e32-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="36e32-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="36e32-110">PARAMETERS</span></span>

### <span data-ttu-id="36e32-111">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36e32-111">CommonParameters</span></span>
<span data-ttu-id="36e32-112">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36e32-112">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36e32-113">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36e32-113">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36e32-114">Eingaben</span><span class="sxs-lookup"><span data-stu-id="36e32-114">INPUTS</span></span>

### <span data-ttu-id="36e32-115">Keine</span><span class="sxs-lookup"><span data-stu-id="36e32-115">None</span></span>


## <span data-ttu-id="36e32-116">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="36e32-116">OUTPUTS</span></span>

### <span data-ttu-id="36e32-117">System. Object</span><span class="sxs-lookup"><span data-stu-id="36e32-117">System.Object</span></span>

## <span data-ttu-id="36e32-118">Notizen</span><span class="sxs-lookup"><span data-stu-id="36e32-118">NOTES</span></span>

## <span data-ttu-id="36e32-119">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="36e32-119">RELATED LINKS</span></span>

