---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdiagnosticdetailsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
ms.openlocfilehash: b990a386feebe8e04ba612c45550ecbd07524c7a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170208"
---
# <span data-ttu-id="08c23-101">New-AzDiagnosticDetailSetting</span><span class="sxs-lookup"><span data-stu-id="08c23-101">New-AzDiagnosticDetailSetting</span></span>

## <span data-ttu-id="08c23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08c23-102">SYNOPSIS</span></span>
<span data-ttu-id="08c23-103">Erstellen Sie das PSDiagnosticDetailSetting-Objekt. Der Typ kann eine Metrik oder ein Protokoll sein.</span><span class="sxs-lookup"><span data-stu-id="08c23-103">Create PSDiagnosticDetailSetting Object, type could be metric or log</span></span>

## <span data-ttu-id="08c23-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="08c23-104">SYNTAX</span></span>

### <span data-ttu-id="08c23-105">LogSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="08c23-105">LogSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Log [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08c23-106">MetricSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="08c23-106">MetricSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Metric [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-TimeGrain <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08c23-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08c23-107">DESCRIPTION</span></span>
<span data-ttu-id="08c23-108">Erstellen Sie ein PSMetricSettings- oder PSLogSettings-Objekt.</span><span class="sxs-lookup"><span data-stu-id="08c23-108">Create PSMetricSettings or PSLogSettings object.</span></span> <span data-ttu-id="08c23-109">Kategorien können Sie mithilfe von `Get-AzDiagnosticSettingCategory` .</span><span class="sxs-lookup"><span data-stu-id="08c23-109">You can get categories by using `Get-AzDiagnosticSettingCategory`.</span></span>

## <span data-ttu-id="08c23-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="08c23-110">EXAMPLES</span></span>

### <span data-ttu-id="08c23-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="08c23-111">Example 1</span></span>
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

<span data-ttu-id="08c23-112">Erstellen Sie ein PSMetricSettings-Objekt.</span><span class="sxs-lookup"><span data-stu-id="08c23-112">Create PSMetricSettings object.</span></span>

### <span data-ttu-id="08c23-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="08c23-113">Example 2</span></span>
```powershell
PS C:\> New-AzDiagnosticDetailSetting -Log -RetentionInDays 1 -RetentionEnabled -Category Audit -Enabled
Category Enabled RetentionPolicy               CategoryType
-------- ------- ---------------               ------------
Audit       True …                                     Logs
```

<span data-ttu-id="08c23-114">Erstellen Sie ein PSLogSettings-Objekt.</span><span class="sxs-lookup"><span data-stu-id="08c23-114">Create PSLogSettings object.</span></span>

## <span data-ttu-id="08c23-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08c23-115">PARAMETERS</span></span>

### <span data-ttu-id="08c23-116">-Category</span><span class="sxs-lookup"><span data-stu-id="08c23-116">-Category</span></span>
<span data-ttu-id="08c23-117">Einstellungskategorie</span><span class="sxs-lookup"><span data-stu-id="08c23-117">Category of setting</span></span>

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

### <span data-ttu-id="08c23-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08c23-118">-DefaultProfile</span></span>
<span data-ttu-id="08c23-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08c23-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08c23-120">-Enabled</span><span class="sxs-lookup"><span data-stu-id="08c23-120">-Enabled</span></span>
<span data-ttu-id="08c23-121">Aktivieren der Einstellung</span><span class="sxs-lookup"><span data-stu-id="08c23-121">Enable the setting</span></span>

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

### <span data-ttu-id="08c23-122">-Log</span><span class="sxs-lookup"><span data-stu-id="08c23-122">-Log</span></span>
<span data-ttu-id="08c23-123">So erstellen Sie eine Protokolleinstellung</span><span class="sxs-lookup"><span data-stu-id="08c23-123">To create log setting</span></span>

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

### <span data-ttu-id="08c23-124">-metrisch</span><span class="sxs-lookup"><span data-stu-id="08c23-124">-Metric</span></span>
<span data-ttu-id="08c23-125">So erstellen Sie eine Metrikeinstellung</span><span class="sxs-lookup"><span data-stu-id="08c23-125">To create metric setting</span></span>

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

### <span data-ttu-id="08c23-126">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="08c23-126">-RetentionEnabled</span></span>
<span data-ttu-id="08c23-127">Aktivieren der Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="08c23-127">Enable Retention policy</span></span>

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

### <span data-ttu-id="08c23-128">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="08c23-128">-RetentionInDays</span></span>
<span data-ttu-id="08c23-129">Aufbewahrungstage für Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="08c23-129">Retention days for retention policy</span></span>

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

### <span data-ttu-id="08c23-130">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="08c23-130">-TimeGrain</span></span>
<span data-ttu-id="08c23-131">TimeGrain für metrische Einstellung</span><span class="sxs-lookup"><span data-stu-id="08c23-131">TimeGrain for metric setting</span></span>

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

### <span data-ttu-id="08c23-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08c23-132">CommonParameters</span></span>
<span data-ttu-id="08c23-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08c23-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08c23-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08c23-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08c23-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="08c23-135">INPUTS</span></span>

### <span data-ttu-id="08c23-136">System.String</span><span class="sxs-lookup"><span data-stu-id="08c23-136">System.String</span></span>

## <span data-ttu-id="08c23-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="08c23-137">OUTPUTS</span></span>

### <span data-ttu-id="08c23-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings</span><span class="sxs-lookup"><span data-stu-id="08c23-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings</span></span>

## <span data-ttu-id="08c23-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="08c23-139">NOTES</span></span>

## <span data-ttu-id="08c23-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="08c23-140">RELATED LINKS</span></span>
