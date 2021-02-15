---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountapiproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
ms.openlocfilehash: 97cf393d0d95dbc9ecfec06f53795713f59aecbd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171342"
---
# <span data-ttu-id="926c6-101">New-AzCognitiveServicesAccountApiProperty</span><span class="sxs-lookup"><span data-stu-id="926c6-101">New-AzCognitiveServicesAccountApiProperty</span></span>

## <span data-ttu-id="926c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="926c6-102">SYNOPSIS</span></span>
<span data-ttu-id="926c6-103">Generieren einer neuen Instanz der Cognitive Services-Konto-ApiProperties</span><span class="sxs-lookup"><span data-stu-id="926c6-103">Generate a new instance of Cognitive Services Account ApiProperties</span></span>

## <span data-ttu-id="926c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="926c6-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountApiProperty [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="926c6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="926c6-105">DESCRIPTION</span></span>
<span data-ttu-id="926c6-106">Generieren Sie eine neue Instanz der Cognitive Services-Konto-ApiProperties.</span><span class="sxs-lookup"><span data-stu-id="926c6-106">Generate a new instance of Cognitive Services Account ApiProperties.</span></span>
<span data-ttu-id="926c6-107">ApiProperties kann beim Erstellen eines neuen Kontos oder Aktualisieren eines vorhandenen Kontos verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="926c6-107">ApiProperties can be used when creating a new account or updating an existing account.</span></span>
<span data-ttu-id="926c6-108">ApiProperties ist für bestimmte Kontotypen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="926c6-108">ApiProperties is required by certain account types.</span></span>

## <span data-ttu-id="926c6-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="926c6-109">EXAMPLES</span></span>

### <span data-ttu-id="926c6-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="926c6-110">Example 1</span></span>
```powershell
PS C:\> $apiProperties = New-AzCognitiveServicesAccountApiProperty
PS C:\> $apiProperties.QnaRuntimeEndpoint = "https://qnamaker.azurewebsites.net"
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name qnamaker -Type QnAMaker -SkuName S0 -Locatio WestUS -ApiProperty $apiProperties
```

<span data-ttu-id="926c6-111">Im obigen Beispiel wird ein QnAMaker-Konto mit der API-Eigenschaft "QnaRuntimeEndpoint" erstellt.</span><span class="sxs-lookup"><span data-stu-id="926c6-111">Above example will create an QnAMaker account, with API property "QnaRuntimeEndpoint".</span></span>


## <span data-ttu-id="926c6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="926c6-112">PARAMETERS</span></span>

### <span data-ttu-id="926c6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="926c6-113">-DefaultProfile</span></span>
<span data-ttu-id="926c6-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="926c6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="926c6-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="926c6-115">-Confirm</span></span>
<span data-ttu-id="926c6-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="926c6-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="926c6-117">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="926c6-117">-WhatIf</span></span>
<span data-ttu-id="926c6-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="926c6-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="926c6-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="926c6-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="926c6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="926c6-120">CommonParameters</span></span>
<span data-ttu-id="926c6-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="926c6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="926c6-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="926c6-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="926c6-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="926c6-123">INPUTS</span></span>

### <span data-ttu-id="926c6-124">Keine</span><span class="sxs-lookup"><span data-stu-id="926c6-124">None</span></span>

## <span data-ttu-id="926c6-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="926c6-125">OUTPUTS</span></span>

### <span data-ttu-id="926c6-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span><span class="sxs-lookup"><span data-stu-id="926c6-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span></span>

## <span data-ttu-id="926c6-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="926c6-127">NOTES</span></span>

## <span data-ttu-id="926c6-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="926c6-128">RELATED LINKS</span></span>
