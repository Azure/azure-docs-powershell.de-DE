---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 349677b4686b2df5a72f233b729a5028dc322057
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93818911"
---
# <span data-ttu-id="18c71-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="18c71-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="18c71-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="18c71-102">SYNOPSIS</span></span>
<span data-ttu-id="18c71-103">Erstellt ein lokales Dimensionsauswahl Objekt, das zum Erstellen einer Metrik für Warnungskriterien verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="18c71-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="18c71-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="18c71-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18c71-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18c71-105">DESCRIPTION</span></span>
<span data-ttu-id="18c71-106">Das Cmdlet **New-AzMetricAlertRuleV2DimensionSelection** erstellt ein lokales Dimensionsauswahl Objekt, das bei der Erstellung von Metrik-Warnungskriterien mithilfe des Cmdlets **New-AzMetricAlertRuleV2Criteria** unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="18c71-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using **New-AzMetricAlertRuleV2Criteria** cmdlet.</span></span>

## <span data-ttu-id="18c71-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="18c71-107">EXAMPLES</span></span>

### <span data-ttu-id="18c71-108">Beispiel 1: Erstellen eines Dimensionsauswahl Objekts</span><span class="sxs-lookup"><span data-stu-id="18c71-108">Example 1 : Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}     
```

<span data-ttu-id="18c71-109">Mit diesem Befehl wird ein Dimensionsauswahl Objekt erstellt, das angibt, dass Werte {1,3,4} für die Dimension "LUN" ausgewählt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="18c71-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="18c71-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="18c71-110">PARAMETERS</span></span>

### <span data-ttu-id="18c71-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18c71-111">-DefaultProfile</span></span>
<span data-ttu-id="18c71-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="18c71-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18c71-113">-Dimensionname</span><span class="sxs-lookup"><span data-stu-id="18c71-113">-DimensionName</span></span>
<span data-ttu-id="18c71-114">Der Dimensionsname</span><span class="sxs-lookup"><span data-stu-id="18c71-114">The Dimension name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18c71-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="18c71-115">-ValuesToExclude</span></span>
<span data-ttu-id="18c71-116">Die ExcludeValues</span><span class="sxs-lookup"><span data-stu-id="18c71-116">The ExcludeValues</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18c71-117">-ValuesToInclude</span><span class="sxs-lookup"><span data-stu-id="18c71-117">-ValuesToInclude</span></span>
<span data-ttu-id="18c71-118">Die IncludeValues</span><span class="sxs-lookup"><span data-stu-id="18c71-118">The IncludeValues</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18c71-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18c71-119">CommonParameters</span></span>
<span data-ttu-id="18c71-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18c71-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="18c71-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18c71-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18c71-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="18c71-122">INPUTS</span></span>

### <span data-ttu-id="18c71-123">System. String</span><span class="sxs-lookup"><span data-stu-id="18c71-123">System.String</span></span>

### <span data-ttu-id="18c71-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="18c71-124">System.String[]</span></span>

## <span data-ttu-id="18c71-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="18c71-125">OUTPUTS</span></span>

### <span data-ttu-id="18c71-126">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDimension</span><span class="sxs-lookup"><span data-stu-id="18c71-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="18c71-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="18c71-127">NOTES</span></span>

## <span data-ttu-id="18c71-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="18c71-128">RELATED LINKS</span></span>
