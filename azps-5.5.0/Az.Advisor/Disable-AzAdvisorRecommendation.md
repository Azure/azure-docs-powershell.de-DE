---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/disable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
ms.openlocfilehash: c9ad0e4b6744c00e9b3f4e7894daa52d2575dd90
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143761"
---
# <span data-ttu-id="3c25f-101">Disable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="3c25f-101">Disable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="3c25f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c25f-102">SYNOPSIS</span></span>
<span data-ttu-id="3c25f-103">Deaktivieren Sie eine Azure Advisor-Empfehlung.</span><span class="sxs-lookup"><span data-stu-id="3c25f-103">Disable an Azure Advisor recommendation.</span></span>

## <span data-ttu-id="3c25f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c25f-104">SYNTAX</span></span>

### <span data-ttu-id="3c25f-105">IdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3c25f-105">IdParameterSet (Default)</span></span>
```
Disable-AzAdvisorRecommendation [-ResourceId] <String> [[-Days] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c25f-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c25f-106">NameParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-RecommendationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c25f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c25f-107">InputObjectParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c25f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3c25f-108">DESCRIPTION</span></span>
<span data-ttu-id="3c25f-109">Dies führt dazu, dass eine bestimmte Empfehlung für eine bestimmte Dauer oder unendlich verschoben werden kann.</span><span class="sxs-lookup"><span data-stu-id="3c25f-109">Creates a suppression for recommendation(s), this enables a particular recommendation to be postponed for a specific duration or infinitely.</span></span>

## <span data-ttu-id="3c25f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3c25f-110">EXAMPLES</span></span>

### <span data-ttu-id="3c25f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3c25f-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -Name "f380a3a8-9d18-cfad-78e0-55762c72a178"

SuppressionId : d1f70547-0e72-db29-443e-c1164d5d4377
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="3c25f-112">Erstellen Sie einen Eintrag für den angegebenen Empfehlungsnamen mit einem Standard-Vornamen und Standardtagen als -1.</span><span class="sxs-lookup"><span data-stu-id="3c25f-112">Create a suppression for the given recommendation name with a default-SuppressionName and default days as -1.</span></span>

### <span data-ttu-id="3c25f-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3c25f-113">Example 2</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" -Days 12

SuppressionId : 7d1f0547-0e72-db29-443e-c1164d5d4377
Ttl           : 12.00:00:00
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="3c25f-114">Für die angegebene Empfehlungs-ID wird ein Vorschlag erstellt.</span><span class="sxs-lookup"><span data-stu-id="3c25f-114">A suppression is created for the given recommendation-Id.</span></span>

### <span data-ttu-id="3c25f-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="3c25f-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzAdvisorRecommendation -ResourceId "/subscriptions/user_subscription/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" | Disable-A
zAdvisorRecommendation

SuppressionId : daf24e78-af2d-e8d3-9c50-fa970edc2937
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="3c25f-116">Erstellen eines ernennenden, von Get-AzAdvisorRecommendation zu Disable-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="3c25f-116">Creating a suppression, piping from Get-AzAdvisorRecommendation to Disable-AzAdvisorRecommendation.</span></span>

## <span data-ttu-id="3c25f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c25f-117">PARAMETERS</span></span>

### <span data-ttu-id="3c25f-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c25f-118">-Confirm</span></span>
<span data-ttu-id="3c25f-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3c25f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c25f-120">-Tage</span><span class="sxs-lookup"><span data-stu-id="3c25f-120">-Days</span></span>
<span data-ttu-id="3c25f-121">Zu deaktivierende Tage.</span><span class="sxs-lookup"><span data-stu-id="3c25f-121">Days to disable.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c25f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c25f-122">-DefaultProfile</span></span>
<span data-ttu-id="3c25f-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3c25f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c25f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c25f-124">-InputObject</span></span>
<span data-ttu-id="3c25f-125">Der von einem Aufruf zurückgegebene "PsAzureAdvisorResourceRecommendationBase" für Get-AzAdvisorRecommendation Powershell-Objekttyp.</span><span class="sxs-lookup"><span data-stu-id="3c25f-125">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

```yaml
Type: PsAzureAdvisorResourceRecommendationBase
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c25f-126">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="3c25f-126">-RecommendationName</span></span>
<span data-ttu-id="3c25f-127">Ressourcenname der Empfehlung</span><span class="sxs-lookup"><span data-stu-id="3c25f-127">ResourceName of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c25f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c25f-128">-ResourceId</span></span>
<span data-ttu-id="3c25f-129">Id der Empfehlung, die unterdrückt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3c25f-129">Id of the recommendation to be suppressed.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c25f-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3c25f-130">-WhatIf</span></span>
<span data-ttu-id="3c25f-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c25f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c25f-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3c25f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c25f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c25f-133">CommonParameters</span></span>
<span data-ttu-id="3c25f-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c25f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3c25f-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c25f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c25f-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3c25f-136">INPUTS</span></span>

### <span data-ttu-id="3c25f-137">System.String</span><span class="sxs-lookup"><span data-stu-id="3c25f-137">System.String</span></span>

### <span data-ttu-id="3c25f-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="3c25f-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="3c25f-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3c25f-139">OUTPUTS</span></span>

### <span data-ttu-id="3c25f-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span><span class="sxs-lookup"><span data-stu-id="3c25f-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span></span>

## <span data-ttu-id="3c25f-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3c25f-141">NOTES</span></span>

## <span data-ttu-id="3c25f-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3c25f-142">RELATED LINKS</span></span>
