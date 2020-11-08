---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/disable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
ms.openlocfilehash: c9ad0e4b6744c00e9b3f4e7894daa52d2575dd90
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996686"
---
# <span data-ttu-id="882d3-101">Disable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="882d3-101">Disable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="882d3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="882d3-102">SYNOPSIS</span></span>
<span data-ttu-id="882d3-103">Deaktivieren Sie eine Azure Advisor-Empfehlung.</span><span class="sxs-lookup"><span data-stu-id="882d3-103">Disable an Azure Advisor recommendation.</span></span>

## <span data-ttu-id="882d3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="882d3-104">SYNTAX</span></span>

### <span data-ttu-id="882d3-105">IdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="882d3-105">IdParameterSet (Default)</span></span>
```
Disable-AzAdvisorRecommendation [-ResourceId] <String> [[-Days] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="882d3-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="882d3-106">NameParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-RecommendationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="882d3-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="882d3-107">InputObjectParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="882d3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="882d3-108">DESCRIPTION</span></span>
<span data-ttu-id="882d3-109">Erstellt eine Unterdrückung für Empfehlung (en), damit kann eine bestimmte Empfehlung auf eine bestimmte Dauer oder unbegrenzt verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="882d3-109">Creates a suppression for recommendation(s), this enables a particular recommendation to be postponed for a specific duration or infinitely.</span></span>

## <span data-ttu-id="882d3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="882d3-110">EXAMPLES</span></span>

### <span data-ttu-id="882d3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="882d3-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -Name "f380a3a8-9d18-cfad-78e0-55762c72a178"

SuppressionId : d1f70547-0e72-db29-443e-c1164d5d4377
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="882d3-112">Erstellen Sie eine Unterdrückung für den angegebenen Empfehlungs Namen mit einem Standard-SuppressionName und Standardtage als-1.</span><span class="sxs-lookup"><span data-stu-id="882d3-112">Create a suppression for the given recommendation name with a default-SuppressionName and default days as -1.</span></span>

### <span data-ttu-id="882d3-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="882d3-113">Example 2</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" -Days 12

SuppressionId : 7d1f0547-0e72-db29-443e-c1164d5d4377
Ttl           : 12.00:00:00
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="882d3-114">Für die angegebene Recommendation-ID wird eine Unterdrückung erstellt.</span><span class="sxs-lookup"><span data-stu-id="882d3-114">A suppression is created for the given recommendation-Id.</span></span>

### <span data-ttu-id="882d3-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="882d3-115">Example 3</span></span>
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

<span data-ttu-id="882d3-116">Erstellen einer Unterdrückung, Piping von Get-AzAdvisorRecommendation zu Disable-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="882d3-116">Creating a suppression, piping from Get-AzAdvisorRecommendation to Disable-AzAdvisorRecommendation.</span></span>

## <span data-ttu-id="882d3-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="882d3-117">PARAMETERS</span></span>

### <span data-ttu-id="882d3-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="882d3-118">-Confirm</span></span>
<span data-ttu-id="882d3-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="882d3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="882d3-120">-Tage</span><span class="sxs-lookup"><span data-stu-id="882d3-120">-Days</span></span>
<span data-ttu-id="882d3-121">Tage, die deaktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="882d3-121">Days to disable.</span></span>

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

### <span data-ttu-id="882d3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="882d3-122">-DefaultProfile</span></span>
<span data-ttu-id="882d3-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="882d3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="882d3-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="882d3-124">-InputObject</span></span>
<span data-ttu-id="882d3-125">Der von Get-AzAdvisorRecommendation Aufruf zurückgegebene PowerShell-Objekttyp PsAzureAdvisorResourceRecommendationBase.</span><span class="sxs-lookup"><span data-stu-id="882d3-125">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="882d3-126">-Recommendation</span><span class="sxs-lookup"><span data-stu-id="882d3-126">-RecommendationName</span></span>
<span data-ttu-id="882d3-127">ResourceName der Empfehlung</span><span class="sxs-lookup"><span data-stu-id="882d3-127">ResourceName of the recommendation</span></span>

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

### <span data-ttu-id="882d3-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="882d3-128">-ResourceId</span></span>
<span data-ttu-id="882d3-129">Die ID der Empfehlung, die unterdrückt werden soll.</span><span class="sxs-lookup"><span data-stu-id="882d3-129">Id of the recommendation to be suppressed.</span></span>

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

### <span data-ttu-id="882d3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="882d3-130">-WhatIf</span></span>
<span data-ttu-id="882d3-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="882d3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="882d3-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="882d3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="882d3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="882d3-133">CommonParameters</span></span>
<span data-ttu-id="882d3-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="882d3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="882d3-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="882d3-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="882d3-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="882d3-136">INPUTS</span></span>

### <span data-ttu-id="882d3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="882d3-137">System.String</span></span>

### <span data-ttu-id="882d3-138">Microsoft. Azure. Commands. Advisor. Cmdlets. Models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="882d3-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="882d3-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="882d3-139">OUTPUTS</span></span>

### <span data-ttu-id="882d3-140">Microsoft. Azure. Commands. Advisor. Cmdlets. Models. PsAzureAdvisorSuppressionContract</span><span class="sxs-lookup"><span data-stu-id="882d3-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span></span>

## <span data-ttu-id="882d3-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="882d3-141">NOTES</span></span>

## <span data-ttu-id="882d3-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="882d3-142">RELATED LINKS</span></span>
