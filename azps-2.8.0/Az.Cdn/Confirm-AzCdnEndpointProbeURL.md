---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/confirm-azcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
ms.openlocfilehash: 517fb30fd95bfc435fcc847a7f9f0765befc21c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652323"
---
# <span data-ttu-id="94a9a-101">Confirm-AzCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="94a9a-101">Confirm-AzCdnEndpointProbeURL</span></span>

## <span data-ttu-id="94a9a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="94a9a-102">SYNOPSIS</span></span>
<span data-ttu-id="94a9a-103">Überprüft eine Prüf Punkt-URL.</span><span class="sxs-lookup"><span data-stu-id="94a9a-103">Validates a probe URL.</span></span>

## <span data-ttu-id="94a9a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="94a9a-104">SYNTAX</span></span>

```
Confirm-AzCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94a9a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94a9a-105">DESCRIPTION</span></span>
<span data-ttu-id="94a9a-106">Das Cmdlet **Confirm-AzCdnEndpointProbeURL** bestätigt, ob die bereitgestellte Prüf Punkt-URL für die dynamische Website Beschleunigung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="94a9a-106">The **Confirm-AzCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="94a9a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="94a9a-107">EXAMPLES</span></span>

### <span data-ttu-id="94a9a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="94a9a-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="94a9a-109">Validiert die Prüf Punkt-URL " http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="94a9a-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="94a9a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="94a9a-110">PARAMETERS</span></span>

### <span data-ttu-id="94a9a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94a9a-111">-DefaultProfile</span></span>
<span data-ttu-id="94a9a-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="94a9a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94a9a-113">-ProbeUrl</span><span class="sxs-lookup"><span data-stu-id="94a9a-113">-ProbeUrl</span></span>
<span data-ttu-id="94a9a-114">Vorgeschlagener Prüfpunkt-URL-Name zur Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="94a9a-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="94a9a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94a9a-115">CommonParameters</span></span>
<span data-ttu-id="94a9a-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94a9a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94a9a-117">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94a9a-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94a9a-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="94a9a-118">INPUTS</span></span>

### <span data-ttu-id="94a9a-119">Keine</span><span class="sxs-lookup"><span data-stu-id="94a9a-119">None</span></span>

## <span data-ttu-id="94a9a-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="94a9a-120">OUTPUTS</span></span>

### <span data-ttu-id="94a9a-121">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="94a9a-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="94a9a-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="94a9a-122">NOTES</span></span>

## <span data-ttu-id="94a9a-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="94a9a-123">RELATED LINKS</span></span>
