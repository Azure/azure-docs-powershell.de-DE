---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/powershell/module/az.advisor/enable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
ms.openlocfilehash: 6bf98fad2b1604f88293b81c55d49e9de3f0c33c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926136"
---
# <span data-ttu-id="bf6e2-101">Enable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="bf6e2-101">Enable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="bf6e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf6e2-102">SYNOPSIS</span></span>
<span data-ttu-id="bf6e2-103">Aktiviert Azure Advisor-Empfehlungen.</span><span class="sxs-lookup"><span data-stu-id="bf6e2-103">Enables Azure Advisor recommendation(s).</span></span>

## <span data-ttu-id="bf6e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf6e2-104">SYNTAX</span></span>

### <span data-ttu-id="bf6e2-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bf6e2-105">NameParameterSet (Default)</span></span>
```
Enable-AzAdvisorRecommendation [-RecommendationName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf6e2-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf6e2-106">IdParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf6e2-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf6e2-107">InputObjectParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf6e2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bf6e2-108">DESCRIPTION</span></span>
<span data-ttu-id="bf6e2-109">Dieses Cmdlet ermöglicht eine zuvor unterdrückte Empfehlung.</span><span class="sxs-lookup"><span data-stu-id="bf6e2-109">This cmdlet enables a previously suppressed recommendation.</span></span> <span data-ttu-id="bf6e2-110">Sie können auch alle einer Empfehlung zugeordneten Löschunterdrückungen entfernen.</span><span class="sxs-lookup"><span data-stu-id="bf6e2-110">You can remove all the suppressions associated with a recommendation as well.</span></span>

## <span data-ttu-id="bf6e2-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bf6e2-111">EXAMPLES</span></span>

### <span data-ttu-id="bf6e2-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bf6e2-112">Example 1</span></span>
```powershell
PS C:\> Enable-AzAdvisorRecommendation -ResourceId c3621337-f131-4bf4-92f2-3fb9c8cfa0d8 

ResourceId           : subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations/c3621337-f131-4bf4-92f2-3fb9c8cfa0d8
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : xyz
LastUpdated          : 12/4/2018 12:06:47 AM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : problem : Improve the performance and reliability of your Redis Cache instance
                       solution : Follow Redis cache Advisor recommendations

SuppressionIds       : {} 
Name                 : c3621337-f131-4bf4-92f2-3fb9c8cfa0d8
Type                 : Microsoft.Advisor/recommendations
```

<span data-ttu-id="bf6e2-113">Entfernt alle Löschunterdrückungen für die angegebene Empfehlung mit dem Namen "recommendation_id".</span><span class="sxs-lookup"><span data-stu-id="bf6e2-113">Removes all the suppressions for the given recommendation with name "recommendation_id".</span></span>

### <span data-ttu-id="bf6e2-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="bf6e2-114">Example 2</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" 
| Enable-AzAdvisorRecommendation

ResourceId           : subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations/{recommendation_id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : xyz
LastUpdated          : 12/4/2018 12:06:47 AM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : problem : Improve the performance and reliability of your Redis Cache instance
                       solution : Follow Redis cache Advisor recommendations

SuppressionIds       : {} 
Name                 : {recommendation_id}
Type                 : Microsoft.Advisor/recommendations
```

<span data-ttu-id="bf6e2-115">Entfernt alle Ausblendungen für die angegebenen Empfehlungen, die von der Pipeline übergeben wurden.</span><span class="sxs-lookup"><span data-stu-id="bf6e2-115">Removes all the suppressions for the given recommendation(s) passed from the pipeline.</span></span>

## <span data-ttu-id="bf6e2-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bf6e2-116">PARAMETERS</span></span>

### <span data-ttu-id="bf6e2-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bf6e2-117">-Confirm</span></span>
<span data-ttu-id="bf6e2-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf6e2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf6e2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf6e2-119">-DefaultProfile</span></span>
<span data-ttu-id="bf6e2-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf6e2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf6e2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf6e2-121">-InputObject</span></span>
<span data-ttu-id="bf6e2-122">Der vom Aufruf zurückgegebene Powershellobjekttyp PsAzureAdvisorResourceRecommendationBase Get-AzAdvisorRecommendation aufruft.</span><span class="sxs-lookup"><span data-stu-id="bf6e2-122">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="bf6e2-123">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="bf6e2-123">-RecommendationName</span></span>
<span data-ttu-id="bf6e2-124">ResourceName der Empfehlung.</span><span class="sxs-lookup"><span data-stu-id="bf6e2-124">ResourceName of the recommendation.</span></span>

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

### <span data-ttu-id="bf6e2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf6e2-125">-ResourceId</span></span>
<span data-ttu-id="bf6e2-126">ID der empfehlung, die unterdrückt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bf6e2-126">Id of the recommendation to be suppressed.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf6e2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf6e2-127">-WhatIf</span></span>
<span data-ttu-id="bf6e2-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf6e2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf6e2-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf6e2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf6e2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf6e2-130">CommonParameters</span></span>
<span data-ttu-id="bf6e2-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf6e2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bf6e2-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf6e2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf6e2-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bf6e2-133">INPUTS</span></span>

### <span data-ttu-id="bf6e2-134">System.String</span><span class="sxs-lookup"><span data-stu-id="bf6e2-134">System.String</span></span>

### <span data-ttu-id="bf6e2-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="bf6e2-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="bf6e2-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bf6e2-136">OUTPUTS</span></span>

### <span data-ttu-id="bf6e2-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="bf6e2-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="bf6e2-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bf6e2-138">NOTES</span></span>

## <span data-ttu-id="bf6e2-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bf6e2-139">RELATED LINKS</span></span>
