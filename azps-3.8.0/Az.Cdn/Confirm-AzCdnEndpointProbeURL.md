---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/confirm-azcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
ms.openlocfilehash: dcd45719754cc8bbb3ef45d8aa9927ae30156937
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995683"
---
# <span data-ttu-id="3840b-101">Confirm-AzCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="3840b-101">Confirm-AzCdnEndpointProbeURL</span></span>

## <span data-ttu-id="3840b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3840b-102">SYNOPSIS</span></span>
<span data-ttu-id="3840b-103">Überprüft eine Prüf Punkt-URL.</span><span class="sxs-lookup"><span data-stu-id="3840b-103">Validates a probe URL.</span></span>

## <span data-ttu-id="3840b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3840b-104">SYNTAX</span></span>

```
Confirm-AzCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3840b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3840b-105">DESCRIPTION</span></span>
<span data-ttu-id="3840b-106">Das Cmdlet **Confirm-AzCdnEndpointProbeURL** bestätigt, ob die bereitgestellte Prüf Punkt-URL für die dynamische Website Beschleunigung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3840b-106">The **Confirm-AzCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="3840b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3840b-107">EXAMPLES</span></span>

### <span data-ttu-id="3840b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3840b-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="3840b-109">Validiert die Prüf Punkt-URL " http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="3840b-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="3840b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3840b-110">PARAMETERS</span></span>

### <span data-ttu-id="3840b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3840b-111">-DefaultProfile</span></span>
<span data-ttu-id="3840b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3840b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3840b-113">-ProbeUrl</span><span class="sxs-lookup"><span data-stu-id="3840b-113">-ProbeUrl</span></span>
<span data-ttu-id="3840b-114">Vorgeschlagener Prüfpunkt-URL-Name zur Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="3840b-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="3840b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3840b-115">CommonParameters</span></span>
<span data-ttu-id="3840b-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3840b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3840b-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3840b-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3840b-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3840b-118">INPUTS</span></span>

### <span data-ttu-id="3840b-119">Keine</span><span class="sxs-lookup"><span data-stu-id="3840b-119">None</span></span>

## <span data-ttu-id="3840b-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3840b-120">OUTPUTS</span></span>

### <span data-ttu-id="3840b-121">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="3840b-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="3840b-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="3840b-122">NOTES</span></span>

## <span data-ttu-id="3840b-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3840b-123">RELATED LINKS</span></span>
