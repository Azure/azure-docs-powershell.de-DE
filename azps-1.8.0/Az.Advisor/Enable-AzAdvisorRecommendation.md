---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/enable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
ms.openlocfilehash: 05d74b254645a970389aae859d60583c53c07670
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650464"
---
# <span data-ttu-id="a8221-101">Enable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="a8221-101">Enable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="a8221-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a8221-102">SYNOPSIS</span></span>
<span data-ttu-id="a8221-103">Aktiviert die Empfehlungen des Azure Advisor (s).</span><span class="sxs-lookup"><span data-stu-id="a8221-103">Enables Azure Advisor recommendation(s).</span></span>

## <span data-ttu-id="a8221-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8221-104">SYNTAX</span></span>

### <span data-ttu-id="a8221-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a8221-105">NameParameterSet (Default)</span></span>
```
Enable-AzAdvisorRecommendation [-RecommendationName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8221-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8221-106">IdParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8221-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8221-107">InputObjectParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8221-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8221-108">DESCRIPTION</span></span>
<span data-ttu-id="a8221-109">Dieses Cmdlet aktiviert eine zuvor unterdrückte Empfehlung.</span><span class="sxs-lookup"><span data-stu-id="a8221-109">This cmdlet enables a previously suppressed recommendation.</span></span> <span data-ttu-id="a8221-110">Sie können auch alle Unterdrückungs Möglichkeiten entfernen, die einer Empfehlung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a8221-110">You can remove all the suppressions associated with a recommendation as well.</span></span>

## <span data-ttu-id="a8221-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8221-111">EXAMPLES</span></span>

### <span data-ttu-id="a8221-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a8221-112">Example 1</span></span>
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

<span data-ttu-id="a8221-113">Entfernt alle Unterdrückungs Angaben für die angegebene Empfehlung mit dem Namen "recommendation_id".</span><span class="sxs-lookup"><span data-stu-id="a8221-113">Removes all the suppressions for the given recommendation with name "recommendation_id".</span></span>

### <span data-ttu-id="a8221-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a8221-114">Example 2</span></span>
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

<span data-ttu-id="a8221-115">Entfernt alle Unterdrückungs Angaben für die angegebene Empfehlung (en), die von der Pipeline übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="a8221-115">Removes all the suppressions for the given recommendation(s) passed from the pipeline.</span></span>

## <span data-ttu-id="a8221-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8221-116">PARAMETERS</span></span>

### <span data-ttu-id="a8221-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a8221-117">-Confirm</span></span>
<span data-ttu-id="a8221-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a8221-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8221-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8221-119">-DefaultProfile</span></span>
<span data-ttu-id="a8221-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a8221-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8221-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a8221-121">-InputObject</span></span>
<span data-ttu-id="a8221-122">Der von Get-AzAdvisorRecommendation Aufruf zurückgegebene PowerShell-Objekttyp PsAzureAdvisorResourceRecommendationBase.</span><span class="sxs-lookup"><span data-stu-id="a8221-122">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="a8221-123">-Recommendation</span><span class="sxs-lookup"><span data-stu-id="a8221-123">-RecommendationName</span></span>
<span data-ttu-id="a8221-124">ResourceName der Empfehlung.</span><span class="sxs-lookup"><span data-stu-id="a8221-124">ResourceName of the recommendation.</span></span>

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

### <span data-ttu-id="a8221-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a8221-125">-ResourceId</span></span>
<span data-ttu-id="a8221-126">Die ID der Empfehlung, die unterdrückt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8221-126">Id of the recommendation to be suppressed.</span></span>

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

### <span data-ttu-id="a8221-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8221-127">-WhatIf</span></span>
<span data-ttu-id="a8221-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a8221-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8221-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a8221-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8221-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8221-130">CommonParameters</span></span>
<span data-ttu-id="a8221-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8221-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a8221-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8221-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8221-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a8221-133">INPUTS</span></span>

### <span data-ttu-id="a8221-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a8221-134">System.String</span></span>

### <span data-ttu-id="a8221-135">Microsoft. Azure. Commands. Advisor. Cmdlets. Models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="a8221-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="a8221-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a8221-136">OUTPUTS</span></span>

### <span data-ttu-id="a8221-137">Microsoft. Azure. Commands. Advisor. Cmdlets. Models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="a8221-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="a8221-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="a8221-138">NOTES</span></span>

## <span data-ttu-id="a8221-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a8221-139">RELATED LINKS</span></span>
