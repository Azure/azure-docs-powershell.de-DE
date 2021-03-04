---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/measure-azalertstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
ms.openlocfilehash: 27fb22a5cded5e196a4bef0aa8b504771abef864
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942739"
---
# <span data-ttu-id="77256-101">Measure-AzAlertStatistic</span><span class="sxs-lookup"><span data-stu-id="77256-101">Measure-AzAlertStatistic</span></span>

## <span data-ttu-id="77256-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77256-102">SYNOPSIS</span></span>
<span data-ttu-id="77256-103">Ruft Benachrichtigungszusammenfassungsinformationen ab</span><span class="sxs-lookup"><span data-stu-id="77256-103">Gets Alert Summary Information</span></span>

## <span data-ttu-id="77256-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="77256-104">SYNTAX</span></span>

### <span data-ttu-id="77256-105">SummaryTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="77256-105">SummaryTargetResourceIdFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceId <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77256-106">SummaryFilter</span><span class="sxs-lookup"><span data-stu-id="77256-106">SummaryFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceType <String>] [-TargetResourceGroup <String>]
 [-MonitorService <String>] [-MonitorCondition <String>] [-Severity <String>] [-State <String>]
 [-AlertRuleId <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77256-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="77256-107">DESCRIPTION</span></span>
<span data-ttu-id="77256-108">**Measure-AzAlertStatistic-Cmdlet** ruft Benachrichtigungszusammenfassungsdetails ab.</span><span class="sxs-lookup"><span data-stu-id="77256-108">**Measure-AzAlertStatistic** cmdlet gets alert summary details.</span></span>

## <span data-ttu-id="77256-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="77256-109">EXAMPLES</span></span>

### <span data-ttu-id="77256-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="77256-110">Example 1</span></span>
```powershell
PS C:\> Measure-AzAlertStatistic -GroupBy "severity,alertstate" -State "Active"
```

<span data-ttu-id="77256-111">Fassen Sie die Anzahl der Benachrichtigungen nach Schweregrad und Status zusammen, die nach dem Status Aktiv gefiltert sind.</span><span class="sxs-lookup"><span data-stu-id="77256-111">Summarize alerts count grouped by severity and state filtered by Active state.</span></span>

## <span data-ttu-id="77256-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="77256-112">PARAMETERS</span></span>

### <span data-ttu-id="77256-113">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="77256-113">-AlertRuleId</span></span>
<span data-ttu-id="77256-114">Filtern nach Warnungsregel-ID</span><span class="sxs-lookup"><span data-stu-id="77256-114">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="77256-115">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="77256-115">-CustomTimeRange</span></span>
<span data-ttu-id="77256-116">Unterstütztes Format : \<start-time\> / \<end-time\> Uhrzeit im ISO-8601-Format</span><span class="sxs-lookup"><span data-stu-id="77256-116">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="77256-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77256-117">-DefaultProfile</span></span>
<span data-ttu-id="77256-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="77256-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77256-119">-GroupBy</span><span class="sxs-lookup"><span data-stu-id="77256-119">-GroupBy</span></span>
<span data-ttu-id="77256-120">Zusammenfassen nach Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="77256-120">Summarize by property</span></span>

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

### <span data-ttu-id="77256-121">-IncludeSmartGroupsCount</span><span class="sxs-lookup"><span data-stu-id="77256-121">-IncludeSmartGroupsCount</span></span>
<span data-ttu-id="77256-122">Zählen von SmartGroups</span><span class="sxs-lookup"><span data-stu-id="77256-122">Include SmartGroups Count</span></span>

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

### <span data-ttu-id="77256-123">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="77256-123">-MonitorCondition</span></span>
<span data-ttu-id="77256-124">Filter nach Monitorbedingung</span><span class="sxs-lookup"><span data-stu-id="77256-124">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="77256-125">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="77256-125">-MonitorService</span></span>
<span data-ttu-id="77256-126">Filtern nach Moniter-Dienst</span><span class="sxs-lookup"><span data-stu-id="77256-126">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="77256-127">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="77256-127">-Severity</span></span>
<span data-ttu-id="77256-128">Filtern nach Schweregrad der Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="77256-128">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="77256-129">-State</span><span class="sxs-lookup"><span data-stu-id="77256-129">-State</span></span>
<span data-ttu-id="77256-130">Filtern nach Benachrichtigungszustand</span><span class="sxs-lookup"><span data-stu-id="77256-130">Filter on State of alert</span></span>

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

### <span data-ttu-id="77256-131">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="77256-131">-TargetResourceGroup</span></span>
<span data-ttu-id="77256-132">Filtern Sie nach dem Namen der Ressourcengruppe der Zielressource der Warnung.</span><span class="sxs-lookup"><span data-stu-id="77256-132">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="77256-133">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="77256-133">-TargetResourceId</span></span>
<span data-ttu-id="77256-134">Filtern Sie nach der Ressourcen-ID der Zielressource der Warnung.</span><span class="sxs-lookup"><span data-stu-id="77256-134">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="77256-135">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="77256-135">-TargetResourceType</span></span>
<span data-ttu-id="77256-136">Filtern Sie nach Ressourcentyp der Zielressource der Warnung.</span><span class="sxs-lookup"><span data-stu-id="77256-136">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="77256-137">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="77256-137">-TimeRange</span></span>
<span data-ttu-id="77256-138">Unterstützte Zeitbereichswerte – 1h, 1d, 7d, 30d (Standard ist 1d)</span><span class="sxs-lookup"><span data-stu-id="77256-138">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="77256-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77256-139">CommonParameters</span></span>
<span data-ttu-id="77256-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77256-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77256-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77256-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77256-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="77256-142">INPUTS</span></span>

### <span data-ttu-id="77256-143">Keine</span><span class="sxs-lookup"><span data-stu-id="77256-143">None</span></span>

## <span data-ttu-id="77256-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="77256-144">OUTPUTS</span></span>

### <span data-ttu-id="77256-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span><span class="sxs-lookup"><span data-stu-id="77256-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span></span>

## <span data-ttu-id="77256-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="77256-146">NOTES</span></span>

## <span data-ttu-id="77256-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="77256-147">RELATED LINKS</span></span>
