---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 33e1b8fe5ae88666ffacf8849b9e2700f7066151
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841972"
---
# <span data-ttu-id="dccc6-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="dccc6-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="dccc6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dccc6-102">SYNOPSIS</span></span>
<span data-ttu-id="dccc6-103">Erstellt ein lokales Dimensionsauswahl Objekt, das zum Erstellen einer Metrik für Warnungskriterien verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="dccc6-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="dccc6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dccc6-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dccc6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dccc6-105">DESCRIPTION</span></span>
<span data-ttu-id="dccc6-106">Das Cmdlet **New-AzMetricAlertRuleV2DimensionSelection** erstellt ein lokales Dimensionsauswahl Objekt, das bei der Erstellung von Metrik-Warnungskriterien mithilfe des Cmdlets **New-AzMetricAlertRuleV2Criteria** unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="dccc6-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using **New-AzMetricAlertRuleV2Criteria** cmdlet.</span></span>

## <span data-ttu-id="dccc6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dccc6-107">EXAMPLES</span></span>

### <span data-ttu-id="dccc6-108">Beispiel 1: Erstellen eines Dimensionsauswahl Objekts</span><span class="sxs-lookup"><span data-stu-id="dccc6-108">Example 1 : Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}
```

<span data-ttu-id="dccc6-109">Mit diesem Befehl wird ein Dimensionsauswahl Objekt erstellt, das angibt, dass Werte {1,3,4} für die Dimension "LUN" ausgewählt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="dccc6-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="dccc6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccc6-110">PARAMETERS</span></span>

### <span data-ttu-id="dccc6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dccc6-111">-DefaultProfile</span></span>
<span data-ttu-id="dccc6-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dccc6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dccc6-113">-Dimensionname</span><span class="sxs-lookup"><span data-stu-id="dccc6-113">-DimensionName</span></span>
<span data-ttu-id="dccc6-114">Der Dimensionsname</span><span class="sxs-lookup"><span data-stu-id="dccc6-114">The Dimension name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccc6-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="dccc6-115">-ValuesToExclude</span></span>
<span data-ttu-id="dccc6-116">Die ExcludeValues</span><span class="sxs-lookup"><span data-stu-id="dccc6-116">The ExcludeValues</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccc6-117">-ValuesToInclude</span><span class="sxs-lookup"><span data-stu-id="dccc6-117">-ValuesToInclude</span></span>
<span data-ttu-id="dccc6-118">Die IncludeValues</span><span class="sxs-lookup"><span data-stu-id="dccc6-118">The IncludeValues</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dccc6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dccc6-119">CommonParameters</span></span>
<span data-ttu-id="dccc6-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dccc6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dccc6-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dccc6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dccc6-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dccc6-122">INPUTS</span></span>

### <span data-ttu-id="dccc6-123">System. String</span><span class="sxs-lookup"><span data-stu-id="dccc6-123">System.String</span></span>

### <span data-ttu-id="dccc6-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="dccc6-124">System.String[]</span></span>

## <span data-ttu-id="dccc6-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dccc6-125">OUTPUTS</span></span>

### <span data-ttu-id="dccc6-126">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDimension</span><span class="sxs-lookup"><span data-stu-id="dccc6-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="dccc6-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="dccc6-127">NOTES</span></span>

## <span data-ttu-id="dccc6-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dccc6-128">RELATED LINKS</span></span>
