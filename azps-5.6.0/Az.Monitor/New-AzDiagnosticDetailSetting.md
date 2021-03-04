---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azdiagnosticdetailsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
ms.openlocfilehash: cccc773adf4b70f0dcef077ea436963c0af9f190
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934899"
---
# <span data-ttu-id="95d37-101">New-AzDiagnosticDetailSetting</span><span class="sxs-lookup"><span data-stu-id="95d37-101">New-AzDiagnosticDetailSetting</span></span>

## <span data-ttu-id="95d37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95d37-102">SYNOPSIS</span></span>
<span data-ttu-id="95d37-103">Erstellen von PSDiagnosticDetailSetting-Objekt, Typ kann Metrik oder Protokoll sein</span><span class="sxs-lookup"><span data-stu-id="95d37-103">Create PSDiagnosticDetailSetting Object, type could be metric or log</span></span>

## <span data-ttu-id="95d37-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95d37-104">SYNTAX</span></span>

### <span data-ttu-id="95d37-105">LogSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="95d37-105">LogSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Log [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95d37-106">MetricSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="95d37-106">MetricSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Metric [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-TimeGrain <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95d37-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95d37-107">DESCRIPTION</span></span>
<span data-ttu-id="95d37-108">Erstellen Sie PSMetricSettings oder PSLogSettings-Objekt.</span><span class="sxs-lookup"><span data-stu-id="95d37-108">Create PSMetricSettings or PSLogSettings object.</span></span> <span data-ttu-id="95d37-109">Sie können Kategorien mithilfe von `Get-AzDiagnosticSettingCategory` erhalten.</span><span class="sxs-lookup"><span data-stu-id="95d37-109">You can get categories by using `Get-AzDiagnosticSettingCategory`.</span></span>

## <span data-ttu-id="95d37-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="95d37-110">EXAMPLES</span></span>

### <span data-ttu-id="95d37-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="95d37-111">Example 1</span></span>
```powershell
PS C:\> $TimeGrain=New-TimeSpan -Days 90
PS C:\> New-AzDiagnosticDetailSetting -Metric -RetentionInDays 1 -RetentionEnabled -Category AllMetrics -Enabled -TimeGrain $TimeGrain
TimeGrain       : 90.00:00:00
Category        : AllMetrics
Enabled         : True
RetentionPolicy :
                  Enabled : True
                  Days    : 1
CategoryType    : Metrics
```

<span data-ttu-id="95d37-112">Erstellen Sie ein PSMetricSettings-Objekt.</span><span class="sxs-lookup"><span data-stu-id="95d37-112">Create PSMetricSettings object.</span></span>

### <span data-ttu-id="95d37-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="95d37-113">Example 2</span></span>
```powershell
PS C:\> New-AzDiagnosticDetailSetting -Log -RetentionInDays 1 -RetentionEnabled -Category Audit -Enabled
Category Enabled RetentionPolicy               CategoryType
-------- ------- ---------------               ------------
Audit       True …                                     Logs
```

<span data-ttu-id="95d37-114">Erstellen Sie das PSLogSettings-Objekt.</span><span class="sxs-lookup"><span data-stu-id="95d37-114">Create PSLogSettings object.</span></span>

## <span data-ttu-id="95d37-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="95d37-115">PARAMETERS</span></span>

### <span data-ttu-id="95d37-116">-Category</span><span class="sxs-lookup"><span data-stu-id="95d37-116">-Category</span></span>
<span data-ttu-id="95d37-117">Kategorie der Einstellung</span><span class="sxs-lookup"><span data-stu-id="95d37-117">Category of setting</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d37-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95d37-118">-DefaultProfile</span></span>
<span data-ttu-id="95d37-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95d37-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95d37-120">-Enabled</span><span class="sxs-lookup"><span data-stu-id="95d37-120">-Enabled</span></span>
<span data-ttu-id="95d37-121">Aktivieren der Einstellung</span><span class="sxs-lookup"><span data-stu-id="95d37-121">Enable the setting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d37-122">-Log</span><span class="sxs-lookup"><span data-stu-id="95d37-122">-Log</span></span>
<span data-ttu-id="95d37-123">So erstellen Sie die Protokolleinstellung</span><span class="sxs-lookup"><span data-stu-id="95d37-123">To create log setting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d37-124">-Metrisch</span><span class="sxs-lookup"><span data-stu-id="95d37-124">-Metric</span></span>
<span data-ttu-id="95d37-125">So erstellen Sie eine Metrikeinstellung</span><span class="sxs-lookup"><span data-stu-id="95d37-125">To create metric setting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MetricSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d37-126">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="95d37-126">-RetentionEnabled</span></span>
<span data-ttu-id="95d37-127">Aktivieren der Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="95d37-127">Enable Retention policy</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d37-128">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="95d37-128">-RetentionInDays</span></span>
<span data-ttu-id="95d37-129">Aufbewahrungstage für Aufbewahrungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="95d37-129">Retention days for retention policy</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d37-130">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="95d37-130">-TimeGrain</span></span>
<span data-ttu-id="95d37-131">Zeitgrain für Metrikeinstellung</span><span class="sxs-lookup"><span data-stu-id="95d37-131">TimeGrain for metric setting</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: MetricSettingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d37-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d37-132">CommonParameters</span></span>
<span data-ttu-id="95d37-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95d37-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d37-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95d37-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d37-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="95d37-135">INPUTS</span></span>

### <span data-ttu-id="95d37-136">System.String</span><span class="sxs-lookup"><span data-stu-id="95d37-136">System.String</span></span>

## <span data-ttu-id="95d37-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="95d37-137">OUTPUTS</span></span>

### <span data-ttu-id="95d37-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings</span><span class="sxs-lookup"><span data-stu-id="95d37-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings</span></span>

## <span data-ttu-id="95d37-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="95d37-139">NOTES</span></span>

## <span data-ttu-id="95d37-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="95d37-140">RELATED LINKS</span></span>
