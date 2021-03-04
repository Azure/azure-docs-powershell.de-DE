---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountapiproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
ms.openlocfilehash: 50e62158d4b24282753c726845e7dd88d492843c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933211"
---
# <span data-ttu-id="7992a-101">New-AzCognitiveServicesAccountApiProperty</span><span class="sxs-lookup"><span data-stu-id="7992a-101">New-AzCognitiveServicesAccountApiProperty</span></span>

## <span data-ttu-id="7992a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7992a-102">SYNOPSIS</span></span>
<span data-ttu-id="7992a-103">Generieren einer neuen Instanz von Cognitive Services Account ApiProperties</span><span class="sxs-lookup"><span data-stu-id="7992a-103">Generate a new instance of Cognitive Services Account ApiProperties</span></span>

## <span data-ttu-id="7992a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7992a-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountApiProperty [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7992a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7992a-105">DESCRIPTION</span></span>
<span data-ttu-id="7992a-106">Generieren Sie eine neue Instanz von Cognitive Services Account ApiProperties.</span><span class="sxs-lookup"><span data-stu-id="7992a-106">Generate a new instance of Cognitive Services Account ApiProperties.</span></span>
<span data-ttu-id="7992a-107">ApiProperties kann beim Erstellen eines neuen Kontos oder beim Aktualisieren eines vorhandenen Kontos verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7992a-107">ApiProperties can be used when creating a new account or updating an existing account.</span></span>
<span data-ttu-id="7992a-108">ApiProperties ist für bestimmte Kontotypen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7992a-108">ApiProperties is required by certain account types.</span></span>

## <span data-ttu-id="7992a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7992a-109">EXAMPLES</span></span>

### <span data-ttu-id="7992a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7992a-110">Example 1</span></span>
```powershell
PS C:\> $apiProperties = New-AzCognitiveServicesAccountApiProperty
PS C:\> $apiProperties.QnaRuntimeEndpoint = "https://qnamaker.azurewebsites.net"
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name qnamaker -Type QnAMaker -SkuName S0 -Locatio WestUS -ApiProperty $apiProperties
```

<span data-ttu-id="7992a-111">Im obigen Beispiel wird ein QnAMaker-Konto mit der API-Eigenschaft "QnaRuntimeEndpoint" erstellt.</span><span class="sxs-lookup"><span data-stu-id="7992a-111">Above example will create an QnAMaker account, with API property "QnaRuntimeEndpoint".</span></span>


## <span data-ttu-id="7992a-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7992a-112">PARAMETERS</span></span>

### <span data-ttu-id="7992a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7992a-113">-DefaultProfile</span></span>
<span data-ttu-id="7992a-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7992a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7992a-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7992a-115">-Confirm</span></span>
<span data-ttu-id="7992a-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7992a-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7992a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7992a-117">-WhatIf</span></span>
<span data-ttu-id="7992a-118">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7992a-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7992a-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7992a-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7992a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7992a-120">CommonParameters</span></span>
<span data-ttu-id="7992a-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7992a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7992a-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7992a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7992a-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7992a-123">INPUTS</span></span>

### <span data-ttu-id="7992a-124">Keine</span><span class="sxs-lookup"><span data-stu-id="7992a-124">None</span></span>

## <span data-ttu-id="7992a-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7992a-125">OUTPUTS</span></span>

### <span data-ttu-id="7992a-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span><span class="sxs-lookup"><span data-stu-id="7992a-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span></span>

## <span data-ttu-id="7992a-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7992a-127">NOTES</span></span>

## <span data-ttu-id="7992a-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7992a-128">RELATED LINKS</span></span>
