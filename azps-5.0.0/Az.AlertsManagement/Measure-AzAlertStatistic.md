---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/measure-azalertstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
ms.openlocfilehash: 96b83f6792babed9fed7c39cad44aec0ea0f26ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175841"
---
# <span data-ttu-id="a79bc-101">Measure-AzAlertStatistic</span><span class="sxs-lookup"><span data-stu-id="a79bc-101">Measure-AzAlertStatistic</span></span>

## <span data-ttu-id="a79bc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a79bc-102">SYNOPSIS</span></span>
<span data-ttu-id="a79bc-103">Ruft Warnungs Zusammenfassungsinformationen ab</span><span class="sxs-lookup"><span data-stu-id="a79bc-103">Gets Alert Summary Information</span></span>

## <span data-ttu-id="a79bc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a79bc-104">SYNTAX</span></span>

### <span data-ttu-id="a79bc-105">SummaryTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="a79bc-105">SummaryTargetResourceIdFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceId <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a79bc-106">SummaryFilter</span><span class="sxs-lookup"><span data-stu-id="a79bc-106">SummaryFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceType <String>] [-TargetResourceGroup <String>]
 [-MonitorService <String>] [-MonitorCondition <String>] [-Severity <String>] [-State <String>]
 [-AlertRuleId <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a79bc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a79bc-107">DESCRIPTION</span></span>
<span data-ttu-id="a79bc-108">**Measure-AzAlertStatistic-** Cmdlet ruft Warnungs Zusammenfassungsdetails ab.</span><span class="sxs-lookup"><span data-stu-id="a79bc-108">**Measure-AzAlertStatistic** cmdlet gets alert summary details.</span></span>

## <span data-ttu-id="a79bc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a79bc-109">EXAMPLES</span></span>

### <span data-ttu-id="a79bc-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a79bc-110">Example 1</span></span>
```powershell
PS C:\> Measure-AzAlertStatistic -GroupBy "severity,alertstate" -State "Active"
```

<span data-ttu-id="a79bc-111">Zusammenfassen von Warnungsanzahl gruppiert nach Schweregrad und Zustand nach aktivem Zustand gefiltert.</span><span class="sxs-lookup"><span data-stu-id="a79bc-111">Summarize alerts count grouped by severity and state filtered by Active state.</span></span>

## <span data-ttu-id="a79bc-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a79bc-112">PARAMETERS</span></span>

### <span data-ttu-id="a79bc-113">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="a79bc-113">-AlertRuleId</span></span>
<span data-ttu-id="a79bc-114">Filtern nach Warnungsregel-ID</span><span class="sxs-lookup"><span data-stu-id="a79bc-114">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="a79bc-115">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="a79bc-115">-CustomTimeRange</span></span>
<span data-ttu-id="a79bc-116">Unterstütztes Format – \<start-time\> / \<end-time\> wobei die Zeit im ISO-8601-Format liegt</span><span class="sxs-lookup"><span data-stu-id="a79bc-116">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="a79bc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a79bc-117">-DefaultProfile</span></span>
<span data-ttu-id="a79bc-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a79bc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a79bc-119">-GroupBy</span><span class="sxs-lookup"><span data-stu-id="a79bc-119">-GroupBy</span></span>
<span data-ttu-id="a79bc-120">Nach Eigenschaft zusammenfassen</span><span class="sxs-lookup"><span data-stu-id="a79bc-120">Summarize by property</span></span>

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

### <span data-ttu-id="a79bc-121">-IncludeSmartGroupsCount</span><span class="sxs-lookup"><span data-stu-id="a79bc-121">-IncludeSmartGroupsCount</span></span>
<span data-ttu-id="a79bc-122">SmartGroups-Anzahl einbeziehen</span><span class="sxs-lookup"><span data-stu-id="a79bc-122">Include SmartGroups Count</span></span>

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

### <span data-ttu-id="a79bc-123">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="a79bc-123">-MonitorCondition</span></span>
<span data-ttu-id="a79bc-124">Filtern nach Monitor Bedingung</span><span class="sxs-lookup"><span data-stu-id="a79bc-124">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="a79bc-125">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="a79bc-125">-MonitorService</span></span>
<span data-ttu-id="a79bc-126">Filter für den Monitordienst</span><span class="sxs-lookup"><span data-stu-id="a79bc-126">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="a79bc-127">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="a79bc-127">-Severity</span></span>
<span data-ttu-id="a79bc-128">Nach Schweregrad der Benachrichtigung Filtern</span><span class="sxs-lookup"><span data-stu-id="a79bc-128">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="a79bc-129">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="a79bc-129">-State</span></span>
<span data-ttu-id="a79bc-130">Nach Warnungsstatus Filtern</span><span class="sxs-lookup"><span data-stu-id="a79bc-130">Filter on State of alert</span></span>

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

### <span data-ttu-id="a79bc-131">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a79bc-131">-TargetResourceGroup</span></span>
<span data-ttu-id="a79bc-132">Filtern nach Ressourcengruppenname der Zielressource für Alert.</span><span class="sxs-lookup"><span data-stu-id="a79bc-132">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="a79bc-133">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="a79bc-133">-TargetResourceId</span></span>
<span data-ttu-id="a79bc-134">Filtern Sie nach der Ressourcen-ID der Zielressource der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="a79bc-134">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="a79bc-135">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="a79bc-135">-TargetResourceType</span></span>
<span data-ttu-id="a79bc-136">Filtern Sie nach dem Ressourcentyp der Zielressource für Alert.</span><span class="sxs-lookup"><span data-stu-id="a79bc-136">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="a79bc-137">-Zeitraum</span><span class="sxs-lookup"><span data-stu-id="a79bc-137">-TimeRange</span></span>
<span data-ttu-id="a79bc-138">Unterstützte Zeitbereichs Werte – 1H, 1D, 7D, 30D (Standard ist 1D)</span><span class="sxs-lookup"><span data-stu-id="a79bc-138">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="a79bc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a79bc-139">CommonParameters</span></span>
<span data-ttu-id="a79bc-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a79bc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a79bc-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a79bc-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a79bc-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a79bc-142">INPUTS</span></span>

### <span data-ttu-id="a79bc-143">Keine</span><span class="sxs-lookup"><span data-stu-id="a79bc-143">None</span></span>

## <span data-ttu-id="a79bc-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a79bc-144">OUTPUTS</span></span>

### <span data-ttu-id="a79bc-145">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlertsSummary</span><span class="sxs-lookup"><span data-stu-id="a79bc-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span></span>

## <span data-ttu-id="a79bc-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="a79bc-146">NOTES</span></span>

## <span data-ttu-id="a79bc-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a79bc-147">RELATED LINKS</span></span>
