---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
ms.openlocfilehash: cf10674f3140e618b82b40e6c8288126cb941c3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480514"
---
# <span data-ttu-id="756a1-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="756a1-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="756a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="756a1-102">SYNOPSIS</span></span>
<span data-ttu-id="756a1-103">Auflisten aller Compute-Ressourcen-SKUs</span><span class="sxs-lookup"><span data-stu-id="756a1-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="756a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="756a1-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="756a1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="756a1-105">DESCRIPTION</span></span>
<span data-ttu-id="756a1-106">Auflisten aller Compute-Ressourcen-SKUs</span><span class="sxs-lookup"><span data-stu-id="756a1-106">List all compute resource Skus</span></span>

## <span data-ttu-id="756a1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="756a1-107">EXAMPLES</span></span>

### <span data-ttu-id="756a1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="756a1-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="756a1-109">Auflisten aller Compute-Ressourcen-SKUs in der Region West-US</span><span class="sxs-lookup"><span data-stu-id="756a1-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="756a1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="756a1-110">PARAMETERS</span></span>

### <span data-ttu-id="756a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="756a1-111">-DefaultProfile</span></span>
<span data-ttu-id="756a1-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="756a1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="756a1-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="756a1-113">CommonParameters</span></span>
<span data-ttu-id="756a1-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="756a1-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="756a1-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="756a1-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="756a1-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="756a1-116">INPUTS</span></span>

### <span data-ttu-id="756a1-117">Keine</span><span class="sxs-lookup"><span data-stu-id="756a1-117">None</span></span>

## <span data-ttu-id="756a1-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="756a1-118">OUTPUTS</span></span>

### <span data-ttu-id="756a1-119">Microsoft. Azure. Commands. Compute. Automation. Models. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="756a1-119">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="756a1-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="756a1-120">NOTES</span></span>

## <span data-ttu-id="756a1-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="756a1-121">RELATED LINKS</span></span>
