---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: d65cd0a5f29f15d2d82227aad6520df34fd4357f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295462"
---
# <span data-ttu-id="47a46-101">Set-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="47a46-101">Set-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="47a46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47a46-102">SYNOPSIS</span></span>
<span data-ttu-id="47a46-103">Erstellt oder aktualisiert einen Sicherheitsbewertungstyp.</span><span class="sxs-lookup"><span data-stu-id="47a46-103">Creates or updates a security assessment type.</span></span>

## <span data-ttu-id="47a46-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47a46-104">SYNTAX</span></span>

```
Set-AzSecurityAssessmentMetadata -Name <String> -DisplayName <String> [-Description <String>]
 [-RemediationDescription <String>] [-Severity <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47a46-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47a46-105">DESCRIPTION</span></span>
<span data-ttu-id="47a46-106">Dient zum Erstellen und Verwalten verschiedener Bewertungseigenschaften, um Metadaten zur Sicherheitsbewertung zu erstellen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="47a46-106">Creates or updates a security assessment metadata, can be used to create and manage various assessment properties.</span></span>
<span data-ttu-id="47a46-107">Nach dieser Aktion können Sie Bewertungsergebnisse für jede Ressource in diesem Abonnement melden.</span><span class="sxs-lookup"><span data-stu-id="47a46-107">After this action you will be able to report assessment results on any resource in this subscription.</span></span>

## <span data-ttu-id="47a46-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="47a46-108">EXAMPLES</span></span>

### <span data-ttu-id="47a46-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="47a46-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessmentMetadata -Name $assessmentGuid -DisplayName "Resource should be secured" -Severity "High" -Description "The resource should be secured according to my company's security policy"
```

<span data-ttu-id="47a46-110">Erstellen Sie einen neuen Bewertungstyp in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="47a46-110">Create a new assessment type in a subscription.</span></span>

## <span data-ttu-id="47a46-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47a46-111">PARAMETERS</span></span>

### <span data-ttu-id="47a46-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47a46-112">-DefaultProfile</span></span>
<span data-ttu-id="47a46-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47a46-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47a46-114">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47a46-114">-Description</span></span>
<span data-ttu-id="47a46-115">Detaillierte Zeichenfolge, die den Benutzern hilft, die Bedeutung dieser Bewertung und deren Berechnung zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="47a46-115">Detailed string that will help users to understand the meaning of this assessment and how it was calculated.</span></span>

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

### <span data-ttu-id="47a46-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="47a46-116">-DisplayName</span></span>
<span data-ttu-id="47a46-117">Lesbarer Titel für dieses Objekt.</span><span class="sxs-lookup"><span data-stu-id="47a46-117">Human readable title for this object.</span></span>

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

### <span data-ttu-id="47a46-118">-Name</span><span class="sxs-lookup"><span data-stu-id="47a46-118">-Name</span></span>
<span data-ttu-id="47a46-119">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="47a46-119">Resource name.</span></span>

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

### <span data-ttu-id="47a46-120">-RemediationDescription</span><span class="sxs-lookup"><span data-stu-id="47a46-120">-RemediationDescription</span></span>
<span data-ttu-id="47a46-121">Detaillierte Zeichenfolge, die Benutzern hilft, die verschiedenen Möglichkeiten zur Entschärftung oder Behebung des Sicherheitsproblems zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="47a46-121">Detailed string that will help users to understand the different ways to mitigate or fix the security issue.</span></span>

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

### <span data-ttu-id="47a46-122">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="47a46-122">-Severity</span></span>
<span data-ttu-id="47a46-123">Gibt die Wichtigkeit des Sicherheitsrisikos an, wenn die Bewertung fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="47a46-123">Indicates the importance of the security risk if the assessment is unhealthy.</span></span>

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

### <span data-ttu-id="47a46-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47a46-124">-Confirm</span></span>
<span data-ttu-id="47a46-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="47a46-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47a46-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="47a46-126">-WhatIf</span></span>
<span data-ttu-id="47a46-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47a46-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47a46-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47a46-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47a46-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47a46-129">CommonParameters</span></span>
<span data-ttu-id="47a46-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47a46-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47a46-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47a46-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47a46-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="47a46-132">INPUTS</span></span>

### <span data-ttu-id="47a46-133">Keine</span><span class="sxs-lookup"><span data-stu-id="47a46-133">None</span></span>

## <span data-ttu-id="47a46-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="47a46-134">OUTPUTS</span></span>

### <span data-ttu-id="47a46-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="47a46-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="47a46-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="47a46-136">NOTES</span></span>

## <span data-ttu-id="47a46-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="47a46-137">RELATED LINKS</span></span>
