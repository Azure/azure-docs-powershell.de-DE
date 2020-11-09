---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountapiproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
ms.openlocfilehash: 97cf393d0d95dbc9ecfec06f53795713f59aecbd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299668"
---
# <span data-ttu-id="afb35-101">New-AzCognitiveServicesAccountApiProperty</span><span class="sxs-lookup"><span data-stu-id="afb35-101">New-AzCognitiveServicesAccountApiProperty</span></span>

## <span data-ttu-id="afb35-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="afb35-102">SYNOPSIS</span></span>
<span data-ttu-id="afb35-103">Generieren einer neuen Instanz des Cognitive Services-Kontos ApiProperties</span><span class="sxs-lookup"><span data-stu-id="afb35-103">Generate a new instance of Cognitive Services Account ApiProperties</span></span>

## <span data-ttu-id="afb35-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="afb35-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountApiProperty [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="afb35-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="afb35-105">DESCRIPTION</span></span>
<span data-ttu-id="afb35-106">Erstellen Sie eine neue Instanz des kognitiven Dienstkonto-ApiProperties.</span><span class="sxs-lookup"><span data-stu-id="afb35-106">Generate a new instance of Cognitive Services Account ApiProperties.</span></span>
<span data-ttu-id="afb35-107">ApiProperties kann verwendet werden, wenn Sie ein neues Konto erstellen oder ein vorhandenes Konto aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="afb35-107">ApiProperties can be used when creating a new account or updating an existing account.</span></span>
<span data-ttu-id="afb35-108">ApiProperties ist für bestimmte Kontotypen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="afb35-108">ApiProperties is required by certain account types.</span></span>

## <span data-ttu-id="afb35-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="afb35-109">EXAMPLES</span></span>

### <span data-ttu-id="afb35-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="afb35-110">Example 1</span></span>
```powershell
PS C:\> $apiProperties = New-AzCognitiveServicesAccountApiProperty
PS C:\> $apiProperties.QnaRuntimeEndpoint = "https://qnamaker.azurewebsites.net"
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name qnamaker -Type QnAMaker -SkuName S0 -Locatio WestUS -ApiProperty $apiProperties
```

<span data-ttu-id="afb35-111">Im obigen Beispiel wird ein QnAMaker-Konto mit API-Eigenschaft "QnaRuntimeEndpoint" erstellt.</span><span class="sxs-lookup"><span data-stu-id="afb35-111">Above example will create an QnAMaker account, with API property "QnaRuntimeEndpoint".</span></span>


## <span data-ttu-id="afb35-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="afb35-112">PARAMETERS</span></span>

### <span data-ttu-id="afb35-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afb35-113">-DefaultProfile</span></span>
<span data-ttu-id="afb35-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="afb35-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afb35-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="afb35-115">-Confirm</span></span>
<span data-ttu-id="afb35-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="afb35-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afb35-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afb35-117">-WhatIf</span></span>
<span data-ttu-id="afb35-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="afb35-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afb35-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="afb35-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afb35-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afb35-120">CommonParameters</span></span>
<span data-ttu-id="afb35-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afb35-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afb35-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="afb35-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afb35-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="afb35-123">INPUTS</span></span>

### <span data-ttu-id="afb35-124">Keine</span><span class="sxs-lookup"><span data-stu-id="afb35-124">None</span></span>

## <span data-ttu-id="afb35-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="afb35-125">OUTPUTS</span></span>

### <span data-ttu-id="afb35-126">Microsoft. Azure. Management. CognitiveServices. Models. CognitiveServicesAccountApiProperties</span><span class="sxs-lookup"><span data-stu-id="afb35-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span></span>

## <span data-ttu-id="afb35-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="afb35-127">NOTES</span></span>

## <span data-ttu-id="afb35-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="afb35-128">RELATED LINKS</span></span>
