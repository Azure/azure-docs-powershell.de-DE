---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
ms.openlocfilehash: 9a227c742892d94417d42be7137f903e17b8b928
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165583"
---
# <span data-ttu-id="74c31-101">Set-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="74c31-101">Set-AzSecurityAssessment</span></span>

## <span data-ttu-id="74c31-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="74c31-102">SYNOPSIS</span></span>
<span data-ttu-id="74c31-103">Erstellen oder Aktualisieren eines Ergebnisses für die Sicherheitsbewertung für eine Ressource</span><span class="sxs-lookup"><span data-stu-id="74c31-103">Create or update a security assessment result on a resource</span></span>

## <span data-ttu-id="74c31-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="74c31-104">SYNTAX</span></span>

### <span data-ttu-id="74c31-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="74c31-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAssessment -Name <String> [-StatusCode <String>] [-StatusCause <String>]
 [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74c31-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="74c31-106">ResourceIdLevelResource</span></span>
```
Set-AzSecurityAssessment -Name <String> -AssessedResourceId <String> -StatusCode <String>
 [-StatusCause <String>] [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74c31-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="74c31-107">DESCRIPTION</span></span>
<span data-ttu-id="74c31-108">Erstellen oder Aktualisieren eines Sicherheits Bewertungsergebnisses für eine Ressource kann verwendet werden, um den Status eines vorhandenen Ergebnisses zu ändern oder zusätzliche Daten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="74c31-108">Create or update a security assessment result on a resource, can be used to change the status of an existing result or add additional data.</span></span>
<span data-ttu-id="74c31-109">kann nur für "CustomerManaged"-Bewertungstypen und erst nach dem Erstellen der übereinstimmenden Bewertungs Metadaten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74c31-109">can only be used for "CustomerManaged" assessment types and only after the matched assessment metadata is created.</span></span>

## <span data-ttu-id="74c31-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="74c31-110">EXAMPLES</span></span>

### <span data-ttu-id="74c31-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="74c31-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D -StatusCode "Unhealthy"
```

<span data-ttu-id="74c31-112">Kennzeichnet das Abonnement Ergebnis als "fehlerhaft" für die Beurteilung des Typs "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" – Weitere Details zum Bewertungstyp finden Sie unter dem assessmentMetadata-Typ.</span><span class="sxs-lookup"><span data-stu-id="74c31-112">Marks the subscription result as "Unhealthy" for assessment of type "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" - more details about the assessment type will be found under the assessmentMetadata type</span></span>

## <span data-ttu-id="74c31-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="74c31-113">PARAMETERS</span></span>

### <span data-ttu-id="74c31-114">-AdditionalData</span><span class="sxs-lookup"><span data-stu-id="74c31-114">-AdditionalData</span></span>
<span data-ttu-id="74c31-115">Daten, die dem Bewertungsergebnis zugeordnet sind, um bessere Untersuchungen oder Status Klarheit zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="74c31-115">Data that is attached to the assessment result for better investigations or status clarity.</span></span>

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

### <span data-ttu-id="74c31-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="74c31-116">-AssessedResourceId</span></span>
<span data-ttu-id="74c31-117">Die vollständige Ressourcen-ID der Ressource, auf der die Bewertung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="74c31-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="74c31-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74c31-118">-DefaultProfile</span></span>
<span data-ttu-id="74c31-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="74c31-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74c31-120">-Name</span><span class="sxs-lookup"><span data-stu-id="74c31-120">-Name</span></span>
<span data-ttu-id="74c31-121">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="74c31-121">Resource name.</span></span>

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

### <span data-ttu-id="74c31-122">-StatusCause</span><span class="sxs-lookup"><span data-stu-id="74c31-122">-StatusCause</span></span>
<span data-ttu-id="74c31-123">Progremmatic-Code für die Ursache des Bewertungsergebnisses.</span><span class="sxs-lookup"><span data-stu-id="74c31-123">Progremmatic code for the cause of the assessment's result.</span></span>

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

### <span data-ttu-id="74c31-124">-Statuscode</span><span class="sxs-lookup"><span data-stu-id="74c31-124">-StatusCode</span></span>
<span data-ttu-id="74c31-125">Progremmatic-Code für das Ergebnis der Bewertung.</span><span class="sxs-lookup"><span data-stu-id="74c31-125">Progremmatic code for the result of the assessment.</span></span>
<span data-ttu-id="74c31-126">kann "gesund", "ungesund" oder "NotApplicable" sein</span><span class="sxs-lookup"><span data-stu-id="74c31-126">can be "Healthy", "Unhealthy" or "NotApplicable"</span></span>

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

### <span data-ttu-id="74c31-127">-StatusDescription</span><span class="sxs-lookup"><span data-stu-id="74c31-127">-StatusDescription</span></span>
<span data-ttu-id="74c31-128">Menschliche lesbare Beschreibung der Ursache des Bewertungsergebnisses.</span><span class="sxs-lookup"><span data-stu-id="74c31-128">Human readable description of the cause of the assessment's result.</span></span>

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

### <span data-ttu-id="74c31-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="74c31-129">-Confirm</span></span>
<span data-ttu-id="74c31-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="74c31-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74c31-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74c31-131">-WhatIf</span></span>
<span data-ttu-id="74c31-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74c31-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74c31-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="74c31-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74c31-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74c31-134">CommonParameters</span></span>
<span data-ttu-id="74c31-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74c31-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74c31-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74c31-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74c31-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="74c31-137">INPUTS</span></span>

### <span data-ttu-id="74c31-138">Keine</span><span class="sxs-lookup"><span data-stu-id="74c31-138">None</span></span>

## <span data-ttu-id="74c31-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="74c31-139">OUTPUTS</span></span>

### <span data-ttu-id="74c31-140">Microsoft. Azure. Commands. Security. Models. Assessments. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="74c31-140">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="74c31-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="74c31-141">NOTES</span></span>

## <span data-ttu-id="74c31-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="74c31-142">RELATED LINKS</span></span>
