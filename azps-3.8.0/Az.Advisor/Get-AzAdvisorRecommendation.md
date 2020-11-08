---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
ms.openlocfilehash: 631e471af79ab5ac567afeafa8103e22ae885ed7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996680"
---
# <span data-ttu-id="67b44-101">Get-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="67b44-101">Get-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="67b44-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="67b44-102">SYNOPSIS</span></span>
<span data-ttu-id="67b44-103">Ruft eine Liste der Azure Advisor-Empfehlungen ab.</span><span class="sxs-lookup"><span data-stu-id="67b44-103">Gets a list of Azure Advisor recommendations.</span></span>

## <span data-ttu-id="67b44-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="67b44-104">SYNTAX</span></span>

### <span data-ttu-id="67b44-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="67b44-105">NameParameterSet (Default)</span></span>
```
Get-AzAdvisorRecommendation [-Category <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67b44-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67b44-106">IdParameterSet</span></span>
```
Get-AzAdvisorRecommendation [-ResourceId] <String> [-Category <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67b44-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67b44-107">DESCRIPTION</span></span>
<span data-ttu-id="67b44-108">Ruft die Liste der Azure Advisor-Empfehlungen ab.</span><span class="sxs-lookup"><span data-stu-id="67b44-108">Obtains the list of Azure Advisor recommendations.</span></span> <span data-ttu-id="67b44-109">Kann nach Kategorie, Ressourcen-ID, Name usw. gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="67b44-109">Can be filtered by Category, resource-ID, name etc.</span></span>

## <span data-ttu-id="67b44-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67b44-110">EXAMPLES</span></span>

### <span data-ttu-id="67b44-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="67b44-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation
ResourceId                   : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommen
                       dations/{recommendation-Id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : azacache
LastUpdated          : 12/5/2018 4:45:55 PM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsRecommendationBaseShortDescription
SuppressionIds       : {}
Name                 : {recommendation-Id}
Type                 : Microsoft.Advisor/recommendations
```
<span data-ttu-id="67b44-112">Ruft die Liste aller Empfehlungen ab.</span><span class="sxs-lookup"><span data-stu-id="67b44-112">Gets the list of all recommendations.</span></span>

### <span data-ttu-id="67b44-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="67b44-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation -Category Performance
ResourceId                   : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommen
                       dations/{recommendation-Id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : azacache
LastUpdated          : 12/5/2018 4:45:55 PM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsRecommendationBaseShortDescription
SuppressionIds       : {}
Name                 : {recommendation-Id}
Type                 : Microsoft.Advisor/recommendations
```
<span data-ttu-id="67b44-114">Ruft die Liste aller Empfehlungen ab, die nach der kategorieleistung gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="67b44-114">Gets the list of all recommendations filtered by category Performance.</span></span>

## <span data-ttu-id="67b44-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="67b44-115">PARAMETERS</span></span>

### <span data-ttu-id="67b44-116">-Kategorie</span><span class="sxs-lookup"><span data-stu-id="67b44-116">-Category</span></span>
<span data-ttu-id="67b44-117">Kategorie der Empfehlung</span><span class="sxs-lookup"><span data-stu-id="67b44-117">Category of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, HighAvailability, Performance, Security, OperationalExcellence

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67b44-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67b44-118">-DefaultProfile</span></span>
<span data-ttu-id="67b44-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="67b44-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67b44-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67b44-120">-ResourceGroupName</span></span>
<span data-ttu-id="67b44-121">Name der ResourceGroup der Empfehlung</span><span class="sxs-lookup"><span data-stu-id="67b44-121">ResourceGroup name of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67b44-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="67b44-122">-ResourceId</span></span>
<span data-ttu-id="67b44-123">Hilfsquelle der Empfehlung</span><span class="sxs-lookup"><span data-stu-id="67b44-123">ResourceId of the recommendation</span></span>

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

### <span data-ttu-id="67b44-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67b44-124">CommonParameters</span></span>
<span data-ttu-id="67b44-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67b44-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="67b44-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67b44-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67b44-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="67b44-127">INPUTS</span></span>

### <span data-ttu-id="67b44-128">System. String</span><span class="sxs-lookup"><span data-stu-id="67b44-128">System.String</span></span>

## <span data-ttu-id="67b44-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="67b44-129">OUTPUTS</span></span>

### <span data-ttu-id="67b44-130">Microsoft. Azure. Commands. Advisor. Cmdlets. Models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="67b44-130">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="67b44-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="67b44-131">NOTES</span></span>

## <span data-ttu-id="67b44-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="67b44-132">RELATED LINKS</span></span>
