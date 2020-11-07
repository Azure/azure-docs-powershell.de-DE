---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcomputeresourcesku
schema: 2.0.0
ms.openlocfilehash: e7ebc6a8e6b59679757f559ff2d09ebaa8c5475f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850943"
---
# <span data-ttu-id="cbc7c-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="cbc7c-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="cbc7c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cbc7c-102">SYNOPSIS</span></span>
<span data-ttu-id="cbc7c-103">Auflisten aller Compute-Ressourcen-SKUs</span><span class="sxs-lookup"><span data-stu-id="cbc7c-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbc7c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cbc7c-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbc7c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cbc7c-105">DESCRIPTION</span></span>
<span data-ttu-id="cbc7c-106">Auflisten aller Compute-Ressourcen-SKUs</span><span class="sxs-lookup"><span data-stu-id="cbc7c-106">List all compute resource Skus</span></span>

## <span data-ttu-id="cbc7c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cbc7c-107">EXAMPLES</span></span>

### <span data-ttu-id="cbc7c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cbc7c-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="cbc7c-109">Auflisten aller Compute-Ressourcen-SKUs in der Region West-US</span><span class="sxs-lookup"><span data-stu-id="cbc7c-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="cbc7c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cbc7c-110">PARAMETERS</span></span>

### <span data-ttu-id="cbc7c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbc7c-111">-DefaultProfile</span></span>
<span data-ttu-id="cbc7c-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cbc7c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbc7c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbc7c-113">CommonParameters</span></span>
<span data-ttu-id="cbc7c-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbc7c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbc7c-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbc7c-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbc7c-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cbc7c-116">INPUTS</span></span>

### <span data-ttu-id="cbc7c-117">Keine</span><span class="sxs-lookup"><span data-stu-id="cbc7c-117">None</span></span>

## <span data-ttu-id="cbc7c-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cbc7c-118">OUTPUTS</span></span>

### <span data-ttu-id="cbc7c-119">System. Object</span><span class="sxs-lookup"><span data-stu-id="cbc7c-119">System.Object</span></span>

## <span data-ttu-id="cbc7c-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="cbc7c-120">NOTES</span></span>

## <span data-ttu-id="cbc7c-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cbc7c-121">RELATED LINKS</span></span>

