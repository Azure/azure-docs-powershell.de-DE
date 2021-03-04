---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: e2b3dd89152b376ac12826eeb342c80486c2c39a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934491"
---
# <span data-ttu-id="a0646-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="a0646-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="a0646-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0646-102">SYNOPSIS</span></span>
<span data-ttu-id="a0646-103">Liste aller Rechenressourcen Skus</span><span class="sxs-lookup"><span data-stu-id="a0646-103">List all compute resource Skus</span></span>

## <span data-ttu-id="a0646-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0646-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0646-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0646-105">DESCRIPTION</span></span>
<span data-ttu-id="a0646-106">Liste aller Rechenressourcen Skus</span><span class="sxs-lookup"><span data-stu-id="a0646-106">List all compute resource Skus</span></span>

## <span data-ttu-id="a0646-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a0646-107">EXAMPLES</span></span>

### <span data-ttu-id="a0646-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a0646-108">Example 1</span></span>
```
PS C:\> Get-AzComputeResourceSku "westus";
```

<span data-ttu-id="a0646-109">Liste aller Rechenressourcenskuss in der Region "USA, Westen"</span><span class="sxs-lookup"><span data-stu-id="a0646-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="a0646-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a0646-110">PARAMETERS</span></span>

### <span data-ttu-id="a0646-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0646-111">-DefaultProfile</span></span>
<span data-ttu-id="a0646-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0646-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0646-113">-Location</span><span class="sxs-lookup"><span data-stu-id="a0646-113">-Location</span></span>
<span data-ttu-id="a0646-114">Gibt einen Speicherort des verfügbaren Skus für die Liste an.</span><span class="sxs-lookup"><span data-stu-id="a0646-114">Specifies a location of the available skus to list.</span></span>

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

### <span data-ttu-id="a0646-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0646-115">CommonParameters</span></span>
<span data-ttu-id="a0646-116">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0646-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0646-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0646-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0646-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a0646-118">INPUTS</span></span>

### <span data-ttu-id="a0646-119">System.String</span><span class="sxs-lookup"><span data-stu-id="a0646-119">System.String</span></span>

## <span data-ttu-id="a0646-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a0646-120">OUTPUTS</span></span>

### <span data-ttu-id="a0646-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="a0646-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="a0646-122">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a0646-122">NOTES</span></span>

## <span data-ttu-id="a0646-123">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a0646-123">RELATED LINKS</span></span>
