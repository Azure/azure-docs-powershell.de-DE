---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/powershell/module/az.advisor/disable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
ms.openlocfilehash: 3695ee9d027733d3adea17797ffbcf669136e66b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926139"
---
# <span data-ttu-id="d1a8b-101">Disable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="d1a8b-101">Disable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="d1a8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1a8b-102">SYNOPSIS</span></span>
<span data-ttu-id="d1a8b-103">Deaktivieren Sie eine Azure Advisor-Empfehlung.</span><span class="sxs-lookup"><span data-stu-id="d1a8b-103">Disable an Azure Advisor recommendation.</span></span>

## <span data-ttu-id="d1a8b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1a8b-104">SYNTAX</span></span>

### <span data-ttu-id="d1a8b-105">IdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d1a8b-105">IdParameterSet (Default)</span></span>
```
Disable-AzAdvisorRecommendation [-ResourceId] <String> [[-Days] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1a8b-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1a8b-106">NameParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-RecommendationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1a8b-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1a8b-107">InputObjectParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1a8b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d1a8b-108">DESCRIPTION</span></span>
<span data-ttu-id="d1a8b-109">Erstellt eine Verdrängung für Empfehlungsempfehlungen. Dadurch kann eine bestimmte Empfehlung für eine bestimmte Dauer oder unendlich verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="d1a8b-109">Creates a suppression for recommendation(s), this enables a particular recommendation to be postponed for a specific duration or infinitely.</span></span>

## <span data-ttu-id="d1a8b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d1a8b-110">EXAMPLES</span></span>

### <span data-ttu-id="d1a8b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d1a8b-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -Name "f380a3a8-9d18-cfad-78e0-55762c72a178"

SuppressionId : d1f70547-0e72-db29-443e-c1164d5d4377
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="d1a8b-112">Erstellen Sie eine Verdrängung für den angegebenen Empfehlungsnamen mit einem Standardunterdrückungsname und Standardtagen als -1.</span><span class="sxs-lookup"><span data-stu-id="d1a8b-112">Create a suppression for the given recommendation name with a default-SuppressionName and default days as -1.</span></span>

### <span data-ttu-id="d1a8b-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d1a8b-113">Example 2</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" -Days 12

SuppressionId : 7d1f0547-0e72-db29-443e-c1164d5d4377
Ttl           : 12.00:00:00
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="d1a8b-114">Für die angegebene Empfehlungs-ID wird eine Verdrängung erstellt.</span><span class="sxs-lookup"><span data-stu-id="d1a8b-114">A suppression is created for the given recommendation-Id.</span></span>

### <span data-ttu-id="d1a8b-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d1a8b-115">Example 3</span></span>
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

<span data-ttu-id="d1a8b-116">Erstellen einer Verdrängung, piping from Get-AzAdvisorRecommendation to Disable-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="d1a8b-116">Creating a suppression, piping from Get-AzAdvisorRecommendation to Disable-AzAdvisorRecommendation.</span></span>

## <span data-ttu-id="d1a8b-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d1a8b-117">PARAMETERS</span></span>

### <span data-ttu-id="d1a8b-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d1a8b-118">-Confirm</span></span>
<span data-ttu-id="d1a8b-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d1a8b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1a8b-120">-Tage</span><span class="sxs-lookup"><span data-stu-id="d1a8b-120">-Days</span></span>
<span data-ttu-id="d1a8b-121">Tage zum Deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d1a8b-121">Days to disable.</span></span>

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

### <span data-ttu-id="d1a8b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1a8b-122">-DefaultProfile</span></span>
<span data-ttu-id="d1a8b-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1a8b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1a8b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1a8b-124">-InputObject</span></span>
<span data-ttu-id="d1a8b-125">Der vom Aufruf zurückgegebene Powershellobjekttyp PsAzureAdvisorResourceRecommendationBase Get-AzAdvisorRecommendation aufruft.</span><span class="sxs-lookup"><span data-stu-id="d1a8b-125">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="d1a8b-126">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="d1a8b-126">-RecommendationName</span></span>
<span data-ttu-id="d1a8b-127">ResourceName der Empfehlung</span><span class="sxs-lookup"><span data-stu-id="d1a8b-127">ResourceName of the recommendation</span></span>

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

### <span data-ttu-id="d1a8b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1a8b-128">-ResourceId</span></span>
<span data-ttu-id="d1a8b-129">ID der empfehlung, die unterdrückt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d1a8b-129">Id of the recommendation to be suppressed.</span></span>

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

### <span data-ttu-id="d1a8b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1a8b-130">-WhatIf</span></span>
<span data-ttu-id="d1a8b-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1a8b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1a8b-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d1a8b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1a8b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1a8b-133">CommonParameters</span></span>
<span data-ttu-id="d1a8b-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1a8b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d1a8b-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1a8b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1a8b-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d1a8b-136">INPUTS</span></span>

### <span data-ttu-id="d1a8b-137">System.String</span><span class="sxs-lookup"><span data-stu-id="d1a8b-137">System.String</span></span>

### <span data-ttu-id="d1a8b-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="d1a8b-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="d1a8b-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d1a8b-139">OUTPUTS</span></span>

### <span data-ttu-id="d1a8b-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span><span class="sxs-lookup"><span data-stu-id="d1a8b-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span></span>

## <span data-ttu-id="d1a8b-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d1a8b-141">NOTES</span></span>

## <span data-ttu-id="d1a8b-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d1a8b-142">RELATED LINKS</span></span>
