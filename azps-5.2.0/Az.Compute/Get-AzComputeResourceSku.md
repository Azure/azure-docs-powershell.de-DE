---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: 970cbb3e03a4934f648df2f6f8c06275a30740de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294755"
---
# <span data-ttu-id="e8919-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="e8919-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="e8919-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8919-102">SYNOPSIS</span></span>
<span data-ttu-id="e8919-103">Auflisten aller Berechnungsressourcen-SKU</span><span class="sxs-lookup"><span data-stu-id="e8919-103">List all compute resource Skus</span></span>

## <span data-ttu-id="e8919-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8919-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8919-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8919-105">DESCRIPTION</span></span>
<span data-ttu-id="e8919-106">Auflisten aller Berechnungsressourcen-SKU</span><span class="sxs-lookup"><span data-stu-id="e8919-106">List all compute resource Skus</span></span>

## <span data-ttu-id="e8919-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e8919-107">EXAMPLES</span></span>

### <span data-ttu-id="e8919-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e8919-108">Example 1</span></span>
```
PS C:\> Get-AzComputeResourceSku "westus";
```

<span data-ttu-id="e8919-109">Auflisten aller Berechnungsressourcen-SKU in der Region "USA, Westen"</span><span class="sxs-lookup"><span data-stu-id="e8919-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="e8919-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8919-110">PARAMETERS</span></span>

### <span data-ttu-id="e8919-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8919-111">-DefaultProfile</span></span>
<span data-ttu-id="e8919-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e8919-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8919-113">-Location</span><span class="sxs-lookup"><span data-stu-id="e8919-113">-Location</span></span>
<span data-ttu-id="e8919-114">Gibt den Speicherort der verfügbaren SKU an, die in einer Liste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e8919-114">Specifies a location of the available skus to list.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8919-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8919-115">CommonParameters</span></span>
<span data-ttu-id="e8919-116">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8919-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8919-117">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8919-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8919-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e8919-118">INPUTS</span></span>

### <span data-ttu-id="e8919-119">System.String</span><span class="sxs-lookup"><span data-stu-id="e8919-119">System.String</span></span>

## <span data-ttu-id="e8919-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e8919-120">OUTPUTS</span></span>

### <span data-ttu-id="e8919-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="e8919-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="e8919-122">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e8919-122">NOTES</span></span>

## <span data-ttu-id="e8919-123">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e8919-123">RELATED LINKS</span></span>
