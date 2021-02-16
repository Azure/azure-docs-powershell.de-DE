---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/confirm-azcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
ms.openlocfilehash: dcd45719754cc8bbb3ef45d8aa9927ae30156937
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149116"
---
# <span data-ttu-id="e252a-101">Confirm-AzCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="e252a-101">Confirm-AzCdnEndpointProbeURL</span></span>

## <span data-ttu-id="e252a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e252a-102">SYNOPSIS</span></span>
<span data-ttu-id="e252a-103">Überprüft eine Probe-URL.</span><span class="sxs-lookup"><span data-stu-id="e252a-103">Validates a probe URL.</span></span>

## <span data-ttu-id="e252a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e252a-104">SYNTAX</span></span>

```
Confirm-AzCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e252a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e252a-105">DESCRIPTION</span></span>
<span data-ttu-id="e252a-106">Das **Cmdlet "Confirm-AzCdnEndpointProbeURL"** bestätigt, ob die bereitgestellte Prüf-URL für die dynamische Websitebeschleunigung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e252a-106">The **Confirm-AzCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="e252a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e252a-107">EXAMPLES</span></span>

### <span data-ttu-id="e252a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e252a-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="e252a-109">Überprüft die Probe-URL " http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="e252a-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="e252a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e252a-110">PARAMETERS</span></span>

### <span data-ttu-id="e252a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e252a-111">-DefaultProfile</span></span>
<span data-ttu-id="e252a-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e252a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e252a-113">-ProbeUrl</span><span class="sxs-lookup"><span data-stu-id="e252a-113">-ProbeUrl</span></span>
<span data-ttu-id="e252a-114">Vorgeschlagener Name der zu überprüfenden Probe-URL.</span><span class="sxs-lookup"><span data-stu-id="e252a-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="e252a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e252a-115">CommonParameters</span></span>
<span data-ttu-id="e252a-116">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e252a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e252a-117">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e252a-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e252a-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e252a-118">INPUTS</span></span>

### <span data-ttu-id="e252a-119">Keine</span><span class="sxs-lookup"><span data-stu-id="e252a-119">None</span></span>

## <span data-ttu-id="e252a-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e252a-120">OUTPUTS</span></span>

### <span data-ttu-id="e252a-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="e252a-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="e252a-122">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e252a-122">NOTES</span></span>

## <span data-ttu-id="e252a-123">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e252a-123">RELATED LINKS</span></span>
