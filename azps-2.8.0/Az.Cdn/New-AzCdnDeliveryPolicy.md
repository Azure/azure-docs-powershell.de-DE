---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
ms.openlocfilehash: 9dcb9720c194fbad4e82607f50132c9bbc5415c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652292"
---
# <span data-ttu-id="af9d0-101">New-AzCdnDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="af9d0-101">New-AzCdnDeliveryPolicy</span></span>

## <span data-ttu-id="af9d0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="af9d0-102">SYNOPSIS</span></span>
<span data-ttu-id="af9d0-103">Erstellt eine Zustellungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="af9d0-103">Creates a delivery policy.</span></span>

## <span data-ttu-id="af9d0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="af9d0-104">SYNTAX</span></span>

```
New-AzCdnDeliveryPolicy [-Description <String>] -Rule <PSDeliveryRule[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af9d0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="af9d0-105">DESCRIPTION</span></span>
<span data-ttu-id="af9d0-106">Das Cmdlet **New-AzCdnDeliveryPolicy** erstellt eine Zustellungs Richtlinie für die Erstellung von CDN-Endpunkten.</span><span class="sxs-lookup"><span data-stu-id="af9d0-106">The **New-AzCdnDeliveryPolicy** cmdlet creates a delivery policy for CDN endpoint creation.</span></span>

## <span data-ttu-id="af9d0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="af9d0-107">EXAMPLES</span></span>

### <span data-ttu-id="af9d0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="af9d0-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryPolicy -Description "Sample Policy" -Rule $rule

Description   Rules
-----------   -----
Sample Policy {rule1}
```

<span data-ttu-id="af9d0-109">Erstellen einer Beispiel Zustellungs Richtlinie</span><span class="sxs-lookup"><span data-stu-id="af9d0-109">Create a sample delivery policy</span></span>

## <span data-ttu-id="af9d0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="af9d0-110">PARAMETERS</span></span>

### <span data-ttu-id="af9d0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af9d0-111">-DefaultProfile</span></span>
<span data-ttu-id="af9d0-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="af9d0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af9d0-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="af9d0-113">-Description</span></span>
<span data-ttu-id="af9d0-114">Beschreibung der Richtlinie</span><span class="sxs-lookup"><span data-stu-id="af9d0-114">Description of the policy</span></span>

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

### <span data-ttu-id="af9d0-115">-Rule</span><span class="sxs-lookup"><span data-stu-id="af9d0-115">-Rule</span></span>
<span data-ttu-id="af9d0-116">Eine Liste der deliveryRules.</span><span class="sxs-lookup"><span data-stu-id="af9d0-116">A list of deliveryRules.</span></span>

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

### <span data-ttu-id="af9d0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af9d0-117">CommonParameters</span></span>
<span data-ttu-id="af9d0-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af9d0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af9d0-119">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af9d0-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af9d0-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="af9d0-120">INPUTS</span></span>

### <span data-ttu-id="af9d0-121">Keine</span><span class="sxs-lookup"><span data-stu-id="af9d0-121">None</span></span>

## <span data-ttu-id="af9d0-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="af9d0-122">OUTPUTS</span></span>

### <span data-ttu-id="af9d0-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="af9d0-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span></span>

## <span data-ttu-id="af9d0-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="af9d0-124">NOTES</span></span>

## <span data-ttu-id="af9d0-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="af9d0-125">RELATED LINKS</span></span>
