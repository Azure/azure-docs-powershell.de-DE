---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/confirm-azcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
ms.openlocfilehash: dcd45719754cc8bbb3ef45d8aa9927ae30156937
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473212"
---
# <span data-ttu-id="59d25-101">Confirm-AzCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="59d25-101">Confirm-AzCdnEndpointProbeURL</span></span>

## <span data-ttu-id="59d25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59d25-102">SYNOPSIS</span></span>
<span data-ttu-id="59d25-103">Überprüft eine Probe-URL.</span><span class="sxs-lookup"><span data-stu-id="59d25-103">Validates a probe URL.</span></span>

## <span data-ttu-id="59d25-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59d25-104">SYNTAX</span></span>

```
Confirm-AzCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59d25-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59d25-105">DESCRIPTION</span></span>
<span data-ttu-id="59d25-106">Das **Cmdlet "Confirm-AzCdnEndpointProbeURL"** bestätigt, ob die bereitgestellte Prüf-URL für die dynamische Websitebeschleunigung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="59d25-106">The **Confirm-AzCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="59d25-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="59d25-107">EXAMPLES</span></span>

### <span data-ttu-id="59d25-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="59d25-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="59d25-109">Überprüft die Probe-URL " http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="59d25-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="59d25-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59d25-110">PARAMETERS</span></span>

### <span data-ttu-id="59d25-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59d25-111">-DefaultProfile</span></span>
<span data-ttu-id="59d25-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59d25-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59d25-113">-ProbeUrl</span><span class="sxs-lookup"><span data-stu-id="59d25-113">-ProbeUrl</span></span>
<span data-ttu-id="59d25-114">Vorgeschlagener Name der zu überprüfenden Probe-URL.</span><span class="sxs-lookup"><span data-stu-id="59d25-114">Proposed probe URL name to validate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d25-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59d25-115">CommonParameters</span></span>
<span data-ttu-id="59d25-116">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59d25-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59d25-117">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59d25-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59d25-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="59d25-118">INPUTS</span></span>

### <span data-ttu-id="59d25-119">Keine</span><span class="sxs-lookup"><span data-stu-id="59d25-119">None</span></span>

## <span data-ttu-id="59d25-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="59d25-120">OUTPUTS</span></span>

### <span data-ttu-id="59d25-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="59d25-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="59d25-122">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="59d25-122">NOTES</span></span>

## <span data-ttu-id="59d25-123">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="59d25-123">RELATED LINKS</span></span>
