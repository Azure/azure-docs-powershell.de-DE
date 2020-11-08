---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/confirm-azcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
ms.openlocfilehash: dcd45719754cc8bbb3ef45d8aa9927ae30156937
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179423"
---
# <span data-ttu-id="ccdda-101">Confirm-AzCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="ccdda-101">Confirm-AzCdnEndpointProbeURL</span></span>

## <span data-ttu-id="ccdda-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ccdda-102">SYNOPSIS</span></span>
<span data-ttu-id="ccdda-103">Überprüft eine Prüf Punkt-URL.</span><span class="sxs-lookup"><span data-stu-id="ccdda-103">Validates a probe URL.</span></span>

## <span data-ttu-id="ccdda-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccdda-104">SYNTAX</span></span>

```
Confirm-AzCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ccdda-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ccdda-105">DESCRIPTION</span></span>
<span data-ttu-id="ccdda-106">Das Cmdlet **Confirm-AzCdnEndpointProbeURL** bestätigt, ob die bereitgestellte Prüf Punkt-URL für die dynamische Website Beschleunigung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ccdda-106">The **Confirm-AzCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="ccdda-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ccdda-107">EXAMPLES</span></span>

### <span data-ttu-id="ccdda-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ccdda-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="ccdda-109">Validiert die Prüf Punkt-URL " http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="ccdda-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="ccdda-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ccdda-110">PARAMETERS</span></span>

### <span data-ttu-id="ccdda-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccdda-111">-DefaultProfile</span></span>
<span data-ttu-id="ccdda-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ccdda-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccdda-113">-ProbeUrl</span><span class="sxs-lookup"><span data-stu-id="ccdda-113">-ProbeUrl</span></span>
<span data-ttu-id="ccdda-114">Vorgeschlagener Prüfpunkt-URL-Name zur Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="ccdda-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="ccdda-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccdda-115">CommonParameters</span></span>
<span data-ttu-id="ccdda-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccdda-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccdda-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ccdda-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccdda-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ccdda-118">INPUTS</span></span>

### <span data-ttu-id="ccdda-119">Keine</span><span class="sxs-lookup"><span data-stu-id="ccdda-119">None</span></span>

## <span data-ttu-id="ccdda-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ccdda-120">OUTPUTS</span></span>

### <span data-ttu-id="ccdda-121">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="ccdda-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="ccdda-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="ccdda-122">NOTES</span></span>

## <span data-ttu-id="ccdda-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ccdda-123">RELATED LINKS</span></span>
