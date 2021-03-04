---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
ms.openlocfilehash: eb9865d69d51fffc7488379bada256a812503a24
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933227"
---
# <span data-ttu-id="b7dd1-101">Get-AzCognitiveServicesAccountSku</span><span class="sxs-lookup"><span data-stu-id="b7dd1-101">Get-AzCognitiveServicesAccountSku</span></span>

## <span data-ttu-id="b7dd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7dd1-102">SYNOPSIS</span></span>
<span data-ttu-id="b7dd1-103">Ruft die verfügbaren SKUs für ein Konto ab.</span><span class="sxs-lookup"><span data-stu-id="b7dd1-103">Gets the available SKUs for an account.</span></span>

## <span data-ttu-id="b7dd1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7dd1-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountSku [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7dd1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b7dd1-105">DESCRIPTION</span></span>
<span data-ttu-id="b7dd1-106">Das **Get-AzCognitiveServicesAccountSku-Cmdlet** ruft die verfügbaren SKUs für ein Cognitive Services-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="b7dd1-106">The **Get-AzCognitiveServicesAccountSku** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="b7dd1-107">Die SKU ist der Stufenplan für ein Konto.</span><span class="sxs-lookup"><span data-stu-id="b7dd1-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="b7dd1-108">Sie definiert den Preis, das Anruflimit und den Zins für das Konto.</span><span class="sxs-lookup"><span data-stu-id="b7dd1-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="b7dd1-109">Die F0 SKU ist ein kostenloser Tarif.</span><span class="sxs-lookup"><span data-stu-id="b7dd1-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="b7dd1-110">Bezahlte Tarife umfassen S0, S1, S2 und so weiter.</span><span class="sxs-lookup"><span data-stu-id="b7dd1-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="b7dd1-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b7dd1-111">EXAMPLES</span></span>

### <span data-ttu-id="b7dd1-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b7dd1-112">Example 1</span></span>
```powershell
PS C:\> (Get-AzCognitiveServicesAccountSku -Type 'TextAnalytics' -Location "westus").Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="b7dd1-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b7dd1-113">PARAMETERS</span></span>

### <span data-ttu-id="b7dd1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7dd1-114">-DefaultProfile</span></span>
<span data-ttu-id="b7dd1-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b7dd1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7dd1-116">-Location</span><span class="sxs-lookup"><span data-stu-id="b7dd1-116">-Location</span></span>
<span data-ttu-id="b7dd1-117">Standort des Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="b7dd1-117">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7dd1-118">-Type</span><span class="sxs-lookup"><span data-stu-id="b7dd1-118">-Type</span></span>
<span data-ttu-id="b7dd1-119">Cognitive Services-Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="b7dd1-119">Cognitive Services Account Type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7dd1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7dd1-120">CommonParameters</span></span>
<span data-ttu-id="b7dd1-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7dd1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7dd1-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7dd1-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7dd1-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b7dd1-123">INPUTS</span></span>

### <span data-ttu-id="b7dd1-124">System.String</span><span class="sxs-lookup"><span data-stu-id="b7dd1-124">System.String</span></span>

## <span data-ttu-id="b7dd1-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b7dd1-125">OUTPUTS</span></span>

### <span data-ttu-id="b7dd1-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span><span class="sxs-lookup"><span data-stu-id="b7dd1-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span></span>

## <span data-ttu-id="b7dd1-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b7dd1-127">NOTES</span></span>

## <span data-ttu-id="b7dd1-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b7dd1-128">RELATED LINKS</span></span>
