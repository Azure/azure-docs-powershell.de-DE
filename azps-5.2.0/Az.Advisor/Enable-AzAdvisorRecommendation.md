---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/enable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
ms.openlocfilehash: 7126a9c8ee11bcb5b32cc47ae31aaf821b171522
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299499"
---
# <span data-ttu-id="351fd-101">Enable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="351fd-101">Enable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="351fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="351fd-102">SYNOPSIS</span></span>
<span data-ttu-id="351fd-103">Aktiviert Azure Advisor Empfehlung(en).</span><span class="sxs-lookup"><span data-stu-id="351fd-103">Enables Azure Advisor recommendation(s).</span></span>

## <span data-ttu-id="351fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="351fd-104">SYNTAX</span></span>

### <span data-ttu-id="351fd-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="351fd-105">NameParameterSet (Default)</span></span>
```
Enable-AzAdvisorRecommendation [-RecommendationName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="351fd-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="351fd-106">IdParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="351fd-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="351fd-107">InputObjectParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="351fd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="351fd-108">DESCRIPTION</span></span>
<span data-ttu-id="351fd-109">Dieses Cmdlet aktiviert eine zuvor unterdrückte Empfehlung.</span><span class="sxs-lookup"><span data-stu-id="351fd-109">This cmdlet enables a previously suppressed recommendation.</span></span> <span data-ttu-id="351fd-110">Sie können auch alle Mitempfehlungen entfernen, die mit einer Empfehlung verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="351fd-110">You can remove all the suppressions associated with a recommendation as well.</span></span>

## <span data-ttu-id="351fd-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="351fd-111">EXAMPLES</span></span>

### <span data-ttu-id="351fd-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="351fd-112">Example 1</span></span>
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

<span data-ttu-id="351fd-113">Entfernt alle Empfehlungen für die angegebene Empfehlung mit dem Namen "recommendation_id".</span><span class="sxs-lookup"><span data-stu-id="351fd-113">Removes all the suppressions for the given recommendation with name "recommendation_id".</span></span>

### <span data-ttu-id="351fd-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="351fd-114">Example 2</span></span>
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

<span data-ttu-id="351fd-115">Entfernt alle Ausblendungen für die gegebene Empfehlung(n), die aus der Pipeline übergeben wurden.</span><span class="sxs-lookup"><span data-stu-id="351fd-115">Removes all the suppressions for the given recommendation(s) passed from the pipeline.</span></span>

## <span data-ttu-id="351fd-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="351fd-116">PARAMETERS</span></span>

### <span data-ttu-id="351fd-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="351fd-117">-Confirm</span></span>
<span data-ttu-id="351fd-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="351fd-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="351fd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="351fd-119">-DefaultProfile</span></span>
<span data-ttu-id="351fd-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="351fd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="351fd-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="351fd-121">-InputObject</span></span>
<span data-ttu-id="351fd-122">Der von einem Aufruf zurückgegebene Powershellobjekttyp PsAzureAdvisorResourceRecommendationBase Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="351fd-122">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="351fd-123">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="351fd-123">-RecommendationName</span></span>
<span data-ttu-id="351fd-124">Ressourcenname der Empfehlung.</span><span class="sxs-lookup"><span data-stu-id="351fd-124">ResourceName of the recommendation.</span></span>

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

### <span data-ttu-id="351fd-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="351fd-125">-ResourceId</span></span>
<span data-ttu-id="351fd-126">Id der Empfehlung, die unterdrückt werden soll.</span><span class="sxs-lookup"><span data-stu-id="351fd-126">Id of the recommendation to be suppressed.</span></span>

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

### <span data-ttu-id="351fd-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="351fd-127">-WhatIf</span></span>
<span data-ttu-id="351fd-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="351fd-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="351fd-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="351fd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="351fd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="351fd-130">CommonParameters</span></span>
<span data-ttu-id="351fd-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="351fd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="351fd-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="351fd-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="351fd-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="351fd-133">INPUTS</span></span>

### <span data-ttu-id="351fd-134">System.String</span><span class="sxs-lookup"><span data-stu-id="351fd-134">System.String</span></span>

### <span data-ttu-id="351fd-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="351fd-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="351fd-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="351fd-136">OUTPUTS</span></span>

### <span data-ttu-id="351fd-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="351fd-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="351fd-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="351fd-138">NOTES</span></span>

## <span data-ttu-id="351fd-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="351fd-139">RELATED LINKS</span></span>
