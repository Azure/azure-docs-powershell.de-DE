---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/confirm-azurermcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Confirm-AzureRmCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Confirm-AzureRmCdnEndpointProbeURL.md
ms.openlocfilehash: d6cf25c352c89592112aaa0a60cf7ba14ff7acf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498394"
---
# <span data-ttu-id="4b803-101">Confirm-AzureRmCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="4b803-101">Confirm-AzureRmCdnEndpointProbeURL</span></span>

## <span data-ttu-id="4b803-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4b803-102">SYNOPSIS</span></span>
<span data-ttu-id="4b803-103">Überprüft eine Prüf Punkt-URL.</span><span class="sxs-lookup"><span data-stu-id="4b803-103">Validates a probe URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b803-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b803-104">SYNTAX</span></span>

```
Confirm-AzureRmCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4b803-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b803-105">DESCRIPTION</span></span>
<span data-ttu-id="4b803-106">Das Cmdlet **Confirm-AzureRmCdnEndpointProbeURL** bestätigt, ob die bereitgestellte Prüf Punkt-URL für die dynamische Website Beschleunigung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4b803-106">The **Confirm-AzureRmCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="4b803-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4b803-107">EXAMPLES</span></span>

### <span data-ttu-id="4b803-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4b803-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzureRmCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="4b803-109">Validiert die Prüf Punkt-URL " http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="4b803-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="4b803-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b803-110">PARAMETERS</span></span>

### <span data-ttu-id="4b803-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b803-111">-DefaultProfile</span></span>
<span data-ttu-id="4b803-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4b803-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b803-113">-ProbeUrl</span><span class="sxs-lookup"><span data-stu-id="4b803-113">-ProbeUrl</span></span>
<span data-ttu-id="4b803-114">Vorgeschlagener Prüfpunkt-URL-Name zur Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="4b803-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="4b803-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b803-115">CommonParameters</span></span>
<span data-ttu-id="4b803-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b803-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b803-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b803-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b803-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4b803-118">INPUTS</span></span>

### <span data-ttu-id="4b803-119">Keine</span><span class="sxs-lookup"><span data-stu-id="4b803-119">None</span></span>

## <span data-ttu-id="4b803-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4b803-120">OUTPUTS</span></span>

### <span data-ttu-id="4b803-121">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="4b803-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="4b803-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="4b803-122">NOTES</span></span>

## <span data-ttu-id="4b803-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4b803-123">RELATED LINKS</span></span>
