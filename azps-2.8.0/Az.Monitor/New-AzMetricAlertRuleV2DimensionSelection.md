---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 04c48c96ee70896f221bfa824c3fefa06ffa89d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822043"
---
# <span data-ttu-id="7df3d-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="7df3d-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="7df3d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7df3d-102">SYNOPSIS</span></span>
<span data-ttu-id="7df3d-103">Erstellt ein lokales Dimensionsauswahl Objekt, das zum Erstellen einer Metrik für Warnungskriterien verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7df3d-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="7df3d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7df3d-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7df3d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7df3d-105">DESCRIPTION</span></span>
<span data-ttu-id="7df3d-106">Das Cmdlet **New-AzMetricAlertRuleV2DimensionSelection** erstellt ein lokales Dimensionsauswahl Objekt, das bei der Erstellung von Metrik-Warnungskriterien mithilfe des Cmdlets **New-AzMetricAlertRuleV2Criteria** unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="7df3d-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using **New-AzMetricAlertRuleV2Criteria** cmdlet.</span></span>

## <span data-ttu-id="7df3d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7df3d-107">EXAMPLES</span></span>

### <span data-ttu-id="7df3d-108">Beispiel 1: Erstellen eines Dimensionsauswahl Objekts</span><span class="sxs-lookup"><span data-stu-id="7df3d-108">Example 1 : Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}
```

<span data-ttu-id="7df3d-109">Mit diesem Befehl wird ein Dimensionsauswahl Objekt erstellt, das angibt, dass Werte {1,3,4} für die Dimension "LUN" ausgewählt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="7df3d-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="7df3d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7df3d-110">PARAMETERS</span></span>

### <span data-ttu-id="7df3d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7df3d-111">-DefaultProfile</span></span>
<span data-ttu-id="7df3d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7df3d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7df3d-113">-Dimensionname</span><span class="sxs-lookup"><span data-stu-id="7df3d-113">-DimensionName</span></span>
<span data-ttu-id="7df3d-114">Der Dimensionsname</span><span class="sxs-lookup"><span data-stu-id="7df3d-114">The Dimension name</span></span>

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

### <span data-ttu-id="7df3d-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="7df3d-115">-ValuesToExclude</span></span>
<span data-ttu-id="7df3d-116">Die ExcludeValues</span><span class="sxs-lookup"><span data-stu-id="7df3d-116">The ExcludeValues</span></span>

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

### <span data-ttu-id="7df3d-117">-ValuesToInclude</span><span class="sxs-lookup"><span data-stu-id="7df3d-117">-ValuesToInclude</span></span>
<span data-ttu-id="7df3d-118">Die IncludeValues</span><span class="sxs-lookup"><span data-stu-id="7df3d-118">The IncludeValues</span></span>

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

### <span data-ttu-id="7df3d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7df3d-119">CommonParameters</span></span>
<span data-ttu-id="7df3d-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7df3d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7df3d-121">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7df3d-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7df3d-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7df3d-122">INPUTS</span></span>

### <span data-ttu-id="7df3d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="7df3d-123">System.String</span></span>

### <span data-ttu-id="7df3d-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="7df3d-124">System.String[]</span></span>

## <span data-ttu-id="7df3d-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7df3d-125">OUTPUTS</span></span>

### <span data-ttu-id="7df3d-126">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDimension</span><span class="sxs-lookup"><span data-stu-id="7df3d-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="7df3d-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="7df3d-127">NOTES</span></span>

## <span data-ttu-id="7df3d-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7df3d-128">RELATED LINKS</span></span>
