---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: e3c33fb3d61479531303389defb0d7ebdbb3fb64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820776"
---
# <span data-ttu-id="246d6-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="246d6-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="246d6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="246d6-102">SYNOPSIS</span></span>
<span data-ttu-id="246d6-103">Auflisten aller Compute-Ressourcen-SKUs</span><span class="sxs-lookup"><span data-stu-id="246d6-103">List all compute resource Skus</span></span>

## <span data-ttu-id="246d6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="246d6-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="246d6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="246d6-105">DESCRIPTION</span></span>
<span data-ttu-id="246d6-106">Auflisten aller Compute-Ressourcen-SKUs</span><span class="sxs-lookup"><span data-stu-id="246d6-106">List all compute resource Skus</span></span>

## <span data-ttu-id="246d6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="246d6-107">EXAMPLES</span></span>

### <span data-ttu-id="246d6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="246d6-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="246d6-109">Auflisten aller Compute-Ressourcen-SKUs in der Region West-US</span><span class="sxs-lookup"><span data-stu-id="246d6-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="246d6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="246d6-110">PARAMETERS</span></span>

### <span data-ttu-id="246d6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="246d6-111">-DefaultProfile</span></span>
<span data-ttu-id="246d6-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="246d6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="246d6-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="246d6-113">CommonParameters</span></span>
<span data-ttu-id="246d6-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="246d6-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="246d6-115">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="246d6-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="246d6-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="246d6-116">INPUTS</span></span>

### <span data-ttu-id="246d6-117">Keine</span><span class="sxs-lookup"><span data-stu-id="246d6-117">None</span></span>

## <span data-ttu-id="246d6-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="246d6-118">OUTPUTS</span></span>

### <span data-ttu-id="246d6-119">Microsoft. Azure. Commands. Compute. Automation. Models. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="246d6-119">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="246d6-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="246d6-120">NOTES</span></span>

## <span data-ttu-id="246d6-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="246d6-121">RELATED LINKS</span></span>
