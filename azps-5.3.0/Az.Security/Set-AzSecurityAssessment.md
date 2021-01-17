---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
ms.openlocfilehash: 9a227c742892d94417d42be7137f903e17b8b928
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459159"
---
# <span data-ttu-id="469ec-101">Set-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="469ec-101">Set-AzSecurityAssessment</span></span>

## <span data-ttu-id="469ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="469ec-102">SYNOPSIS</span></span>
<span data-ttu-id="469ec-103">Erstellen oder Aktualisieren eines Sicherheitsbewertungsergebniss für eine Ressource</span><span class="sxs-lookup"><span data-stu-id="469ec-103">Create or update a security assessment result on a resource</span></span>

## <span data-ttu-id="469ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="469ec-104">SYNTAX</span></span>

### <span data-ttu-id="469ec-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="469ec-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAssessment -Name <String> [-StatusCode <String>] [-StatusCause <String>]
 [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="469ec-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="469ec-106">ResourceIdLevelResource</span></span>
```
Set-AzSecurityAssessment -Name <String> -AssessedResourceId <String> -StatusCode <String>
 [-StatusCause <String>] [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="469ec-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="469ec-107">DESCRIPTION</span></span>
<span data-ttu-id="469ec-108">Sie können ein Sicherheitsbewertungsergebnis für eine Ressource erstellen oder aktualisieren, um den Status eines vorhandenen Ergebnisses zu ändern oder zusätzliche Daten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="469ec-108">Create or update a security assessment result on a resource, can be used to change the status of an existing result or add additional data.</span></span>
<span data-ttu-id="469ec-109">können nur für Bewertungstypen vom Typ "CustomerManaged" und erst nach dem Erstellen der übereinstimmende Bewertungsmetadaten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="469ec-109">can only be used for "CustomerManaged" assessment types and only after the matched assessment metadata is created.</span></span>

## <span data-ttu-id="469ec-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="469ec-110">EXAMPLES</span></span>

### <span data-ttu-id="469ec-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="469ec-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D -StatusCode "Unhealthy"
```

<span data-ttu-id="469ec-112">Kennzeichnet das Abonnementergebnis als "fehlerhaft" für die Bewertung vom Typ "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D". Weitere Details zum Bewertungstyp finden Sie unter dem Bewertungsmetadata-Typ.</span><span class="sxs-lookup"><span data-stu-id="469ec-112">Marks the subscription result as "Unhealthy" for assessment of type "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" - more details about the assessment type will be found under the assessmentMetadata type</span></span>

## <span data-ttu-id="469ec-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="469ec-113">PARAMETERS</span></span>

### <span data-ttu-id="469ec-114">-AdditionalData</span><span class="sxs-lookup"><span data-stu-id="469ec-114">-AdditionalData</span></span>
<span data-ttu-id="469ec-115">Daten, die an das Bewertungsergebnis angefügt werden, um bessere Untersuchungen oder Klarheit des Status zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="469ec-115">Data that is attached to the assessment result for better investigations or status clarity.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469ec-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="469ec-116">-AssessedResourceId</span></span>
<span data-ttu-id="469ec-117">Vollständige Ressourcen-ID der Ressource, für die die Bewertung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="469ec-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469ec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="469ec-118">-DefaultProfile</span></span>
<span data-ttu-id="469ec-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="469ec-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="469ec-120">-Name</span><span class="sxs-lookup"><span data-stu-id="469ec-120">-Name</span></span>
<span data-ttu-id="469ec-121">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="469ec-121">Resource name.</span></span>

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

### <span data-ttu-id="469ec-122">-StatusCause</span><span class="sxs-lookup"><span data-stu-id="469ec-122">-StatusCause</span></span>
<span data-ttu-id="469ec-123">Progremmatic code for the cause of the assessment's result.</span><span class="sxs-lookup"><span data-stu-id="469ec-123">Progremmatic code for the cause of the assessment's result.</span></span>

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

### <span data-ttu-id="469ec-124">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="469ec-124">-StatusCode</span></span>
<span data-ttu-id="469ec-125">Progremmatic code for the result of the assessment.</span><span class="sxs-lookup"><span data-stu-id="469ec-125">Progremmatic code for the result of the assessment.</span></span>
<span data-ttu-id="469ec-126">können "Fehlerfrei", "fehlerhaft" oder "Nicht anwendbar" sein.</span><span class="sxs-lookup"><span data-stu-id="469ec-126">can be "Healthy", "Unhealthy" or "NotApplicable"</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469ec-127">-StatusDescription</span><span class="sxs-lookup"><span data-stu-id="469ec-127">-StatusDescription</span></span>
<span data-ttu-id="469ec-128">Eine vom Menschen lesbare Beschreibung der Ursache des Bewertungsergebniss.</span><span class="sxs-lookup"><span data-stu-id="469ec-128">Human readable description of the cause of the assessment's result.</span></span>

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

### <span data-ttu-id="469ec-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="469ec-129">-Confirm</span></span>
<span data-ttu-id="469ec-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="469ec-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="469ec-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="469ec-131">-WhatIf</span></span>
<span data-ttu-id="469ec-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="469ec-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="469ec-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="469ec-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="469ec-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="469ec-134">CommonParameters</span></span>
<span data-ttu-id="469ec-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="469ec-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="469ec-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="469ec-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="469ec-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="469ec-137">INPUTS</span></span>

### <span data-ttu-id="469ec-138">Keine</span><span class="sxs-lookup"><span data-stu-id="469ec-138">None</span></span>

## <span data-ttu-id="469ec-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="469ec-139">OUTPUTS</span></span>

### <span data-ttu-id="469ec-140">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="469ec-140">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="469ec-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="469ec-141">NOTES</span></span>

## <span data-ttu-id="469ec-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="469ec-142">RELATED LINKS</span></span>
