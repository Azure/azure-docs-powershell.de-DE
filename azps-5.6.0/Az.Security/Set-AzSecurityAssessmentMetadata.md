---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: e72766e754394bb43775f73072941dc0d3989c3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936043"
---
# <span data-ttu-id="a0f55-101">Set-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="a0f55-101">Set-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="a0f55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0f55-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f55-103">Erstellt oder aktualisiert einen Sicherheitsbewertungstyp.</span><span class="sxs-lookup"><span data-stu-id="a0f55-103">Creates or updates a security assessment type.</span></span>

## <span data-ttu-id="a0f55-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0f55-104">SYNTAX</span></span>

```
Set-AzSecurityAssessmentMetadata -Name <String> -DisplayName <String> [-Description <String>]
 [-RemediationDescription <String>] [-Severity <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0f55-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0f55-105">DESCRIPTION</span></span>
<span data-ttu-id="a0f55-106">Erstellt oder aktualisiert metadaten für die Sicherheitsbewertung, kann verwendet werden, um verschiedene Bewertungseigenschaften zu erstellen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="a0f55-106">Creates or updates a security assessment metadata, can be used to create and manage various assessment properties.</span></span>
<span data-ttu-id="a0f55-107">Nach dieser Aktion können Sie Bewertungsergebnisse für jede Ressource in diesem Abonnement melden.</span><span class="sxs-lookup"><span data-stu-id="a0f55-107">After this action you will be able to report assessment results on any resource in this subscription.</span></span>

## <span data-ttu-id="a0f55-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a0f55-108">EXAMPLES</span></span>

### <span data-ttu-id="a0f55-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a0f55-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessmentMetadata -Name $assessmentGuid -DisplayName "Resource should be secured" -Severity "High" -Description "The resource should be secured according to my company's security policy"
```

<span data-ttu-id="a0f55-110">Erstellen Sie einen neuen Bewertungstyp in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a0f55-110">Create a new assessment type in a subscription.</span></span>

## <span data-ttu-id="a0f55-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a0f55-111">PARAMETERS</span></span>

### <span data-ttu-id="a0f55-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0f55-112">-DefaultProfile</span></span>
<span data-ttu-id="a0f55-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0f55-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0f55-114">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0f55-114">-Description</span></span>
<span data-ttu-id="a0f55-115">Detaillierte Zeichenfolge, die Benutzern dabei hilft, die Bedeutung dieser Bewertung und deren Berechnung zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="a0f55-115">Detailed string that will help users to understand the meaning of this assessment and how it was calculated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f55-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a0f55-116">-DisplayName</span></span>
<span data-ttu-id="a0f55-117">Lesbarer Titel für dieses Objekt für den Menschen.</span><span class="sxs-lookup"><span data-stu-id="a0f55-117">Human readable title for this object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f55-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a0f55-118">-Name</span></span>
<span data-ttu-id="a0f55-119">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="a0f55-119">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f55-120">-RemediationDescription</span><span class="sxs-lookup"><span data-stu-id="a0f55-120">-RemediationDescription</span></span>
<span data-ttu-id="a0f55-121">Detaillierte Zeichenfolge, die Benutzern dabei hilft, die verschiedenen Möglichkeiten zum Verringern oder Beheben des Sicherheitsproblems zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="a0f55-121">Detailed string that will help users to understand the different ways to mitigate or fix the security issue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f55-122">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="a0f55-122">-Severity</span></span>
<span data-ttu-id="a0f55-123">Gibt die Wichtigkeit des Sicherheitsrisikos an, wenn die Bewertung fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="a0f55-123">Indicates the importance of the security risk if the assessment is unhealthy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f55-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a0f55-124">-Confirm</span></span>
<span data-ttu-id="a0f55-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a0f55-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0f55-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0f55-126">-WhatIf</span></span>
<span data-ttu-id="a0f55-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0f55-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0f55-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0f55-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0f55-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f55-129">CommonParameters</span></span>
<span data-ttu-id="a0f55-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0f55-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f55-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0f55-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f55-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a0f55-132">INPUTS</span></span>

### <span data-ttu-id="a0f55-133">Keine</span><span class="sxs-lookup"><span data-stu-id="a0f55-133">None</span></span>

## <span data-ttu-id="a0f55-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a0f55-134">OUTPUTS</span></span>

### <span data-ttu-id="a0f55-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="a0f55-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="a0f55-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a0f55-136">NOTES</span></span>

## <span data-ttu-id="a0f55-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a0f55-137">RELATED LINKS</span></span>
