---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/measure-azalertstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
ms.openlocfilehash: 96b83f6792babed9fed7c39cad44aec0ea0f26ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171984"
---
# <span data-ttu-id="ea650-101">Measure-AzAlertStatistic</span><span class="sxs-lookup"><span data-stu-id="ea650-101">Measure-AzAlertStatistic</span></span>

## <span data-ttu-id="ea650-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea650-102">SYNOPSIS</span></span>
<span data-ttu-id="ea650-103">Ruft Benachrichtigungszusammenfassungsinformationen ab</span><span class="sxs-lookup"><span data-stu-id="ea650-103">Gets Alert Summary Information</span></span>

## <span data-ttu-id="ea650-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea650-104">SYNTAX</span></span>

### <span data-ttu-id="ea650-105">SummaryTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="ea650-105">SummaryTargetResourceIdFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceId <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea650-106">SummaryFilter</span><span class="sxs-lookup"><span data-stu-id="ea650-106">SummaryFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceType <String>] [-TargetResourceGroup <String>]
 [-MonitorService <String>] [-MonitorCondition <String>] [-Severity <String>] [-State <String>]
 [-AlertRuleId <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea650-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea650-107">DESCRIPTION</span></span>
<span data-ttu-id="ea650-108">**Das Cmdlet "Measure-AzAlertStatistic"** erhält Warnungszusammenfassungsdetails.</span><span class="sxs-lookup"><span data-stu-id="ea650-108">**Measure-AzAlertStatistic** cmdlet gets alert summary details.</span></span>

## <span data-ttu-id="ea650-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ea650-109">EXAMPLES</span></span>

### <span data-ttu-id="ea650-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ea650-110">Example 1</span></span>
```powershell
PS C:\> Measure-AzAlertStatistic -GroupBy "severity,alertstate" -State "Active"
```

<span data-ttu-id="ea650-111">Fassen Sie die Anzahl der Warnungen nach Schweregrad und Status, nach dem Status "Aktiv" gefiltert, zusammen.</span><span class="sxs-lookup"><span data-stu-id="ea650-111">Summarize alerts count grouped by severity and state filtered by Active state.</span></span>

## <span data-ttu-id="ea650-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea650-112">PARAMETERS</span></span>

### <span data-ttu-id="ea650-113">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="ea650-113">-AlertRuleId</span></span>
<span data-ttu-id="ea650-114">Filtern nach Warnungsregel-ID</span><span class="sxs-lookup"><span data-stu-id="ea650-114">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea650-115">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="ea650-115">-CustomTimeRange</span></span>
<span data-ttu-id="ea650-116">Unterstütztes Format – \<start-time\> / \<end-time\> Uhrzeit im ISO-8601-Format</span><span class="sxs-lookup"><span data-stu-id="ea650-116">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea650-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea650-117">-DefaultProfile</span></span>
<span data-ttu-id="ea650-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea650-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea650-119">-GroupBy</span><span class="sxs-lookup"><span data-stu-id="ea650-119">-GroupBy</span></span>
<span data-ttu-id="ea650-120">Zusammenfassen nach Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ea650-120">Summarize by property</span></span>

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

### <span data-ttu-id="ea650-121">-IncludeGroupsCount</span><span class="sxs-lookup"><span data-stu-id="ea650-121">-IncludeSmartGroupsCount</span></span>
<span data-ttu-id="ea650-122">SmartGroups Count mitzählen</span><span class="sxs-lookup"><span data-stu-id="ea650-122">Include SmartGroups Count</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea650-123">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="ea650-123">-MonitorCondition</span></span>
<span data-ttu-id="ea650-124">Filter on Monitor Condition</span><span class="sxs-lookup"><span data-stu-id="ea650-124">Filter on Monitor Condition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea650-125">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="ea650-125">-MonitorService</span></span>
<span data-ttu-id="ea650-126">Filtern nach Moniter Service</span><span class="sxs-lookup"><span data-stu-id="ea650-126">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea650-127">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="ea650-127">-Severity</span></span>
<span data-ttu-id="ea650-128">Filtern nach Schweregrad der Warnung</span><span class="sxs-lookup"><span data-stu-id="ea650-128">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea650-129">-State</span><span class="sxs-lookup"><span data-stu-id="ea650-129">-State</span></span>
<span data-ttu-id="ea650-130">Filtern nach Benachrichtigungsstatus</span><span class="sxs-lookup"><span data-stu-id="ea650-130">Filter on State of alert</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea650-131">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ea650-131">-TargetResourceGroup</span></span>
<span data-ttu-id="ea650-132">Filtern Sie nach dem Namen der Ressourcengruppe der zu warnende Zielressource.</span><span class="sxs-lookup"><span data-stu-id="ea650-132">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea650-133">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="ea650-133">-TargetResourceId</span></span>
<span data-ttu-id="ea650-134">Filtern Sie nach der Ressourcen-ID der zu warnende Zielressource.</span><span class="sxs-lookup"><span data-stu-id="ea650-134">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea650-135">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="ea650-135">-TargetResourceType</span></span>
<span data-ttu-id="ea650-136">Filtern Sie nach dem Ressourcentyp der zu warnende Zielressource.</span><span class="sxs-lookup"><span data-stu-id="ea650-136">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea650-137">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="ea650-137">-TimeRange</span></span>
<span data-ttu-id="ea650-138">Unterstützte Zeitbereichswerte – 1h, 1d, 7d, 30d (Standard ist 1d)</span><span class="sxs-lookup"><span data-stu-id="ea650-138">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea650-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea650-139">CommonParameters</span></span>
<span data-ttu-id="ea650-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea650-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea650-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea650-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea650-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ea650-142">INPUTS</span></span>

### <span data-ttu-id="ea650-143">Keine</span><span class="sxs-lookup"><span data-stu-id="ea650-143">None</span></span>

## <span data-ttu-id="ea650-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ea650-144">OUTPUTS</span></span>

### <span data-ttu-id="ea650-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span><span class="sxs-lookup"><span data-stu-id="ea650-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span></span>

## <span data-ttu-id="ea650-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ea650-146">NOTES</span></span>

## <span data-ttu-id="ea650-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ea650-147">RELATED LINKS</span></span>
