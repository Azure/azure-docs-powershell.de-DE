---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
ms.openlocfilehash: a00e8d11868ae487357f1105d2bc2ae3934a9db9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368471"
---
# <span data-ttu-id="f90de-101">New-AzCdnDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="f90de-101">New-AzCdnDeliveryPolicy</span></span>

## <span data-ttu-id="f90de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f90de-102">SYNOPSIS</span></span>
<span data-ttu-id="f90de-103">Erstellt eine Zustellungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="f90de-103">Creates a delivery policy.</span></span>

## <span data-ttu-id="f90de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f90de-104">SYNTAX</span></span>

```
New-AzCdnDeliveryPolicy [-Description <String>] -Rule <PSDeliveryRule[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f90de-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f90de-105">DESCRIPTION</span></span>
<span data-ttu-id="f90de-106">Das **Cmdlet "New-AzCdnDeliveryPolicy"** erstellt eine Zustellungsrichtlinie für die Erstellung von CDN-Endpunkten.</span><span class="sxs-lookup"><span data-stu-id="f90de-106">The **New-AzCdnDeliveryPolicy** cmdlet creates a delivery policy for CDN endpoint creation.</span></span>

## <span data-ttu-id="f90de-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f90de-107">EXAMPLES</span></span>

### <span data-ttu-id="f90de-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f90de-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryPolicy -Description "Sample Policy" -Rule $rule

Description   Rules
-----------   -----
Sample Policy {rule1}
```

<span data-ttu-id="f90de-109">Erstellen einer Beispielzustellungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="f90de-109">Create a sample delivery policy</span></span>

## <span data-ttu-id="f90de-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f90de-110">PARAMETERS</span></span>

### <span data-ttu-id="f90de-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f90de-111">-DefaultProfile</span></span>
<span data-ttu-id="f90de-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f90de-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f90de-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f90de-113">-Description</span></span>
<span data-ttu-id="f90de-114">Beschreibung der Richtlinie</span><span class="sxs-lookup"><span data-stu-id="f90de-114">Description of the policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f90de-115">-Rule</span><span class="sxs-lookup"><span data-stu-id="f90de-115">-Rule</span></span>
<span data-ttu-id="f90de-116">Eine Liste der deliveryRules.</span><span class="sxs-lookup"><span data-stu-id="f90de-116">A list of deliveryRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f90de-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f90de-117">CommonParameters</span></span>
<span data-ttu-id="f90de-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f90de-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f90de-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f90de-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f90de-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f90de-120">INPUTS</span></span>

### <span data-ttu-id="f90de-121">Keine</span><span class="sxs-lookup"><span data-stu-id="f90de-121">None</span></span>

## <span data-ttu-id="f90de-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f90de-122">OUTPUTS</span></span>

### <span data-ttu-id="f90de-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="f90de-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span></span>

## <span data-ttu-id="f90de-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f90de-124">NOTES</span></span>

## <span data-ttu-id="f90de-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f90de-125">RELATED LINKS</span></span>
