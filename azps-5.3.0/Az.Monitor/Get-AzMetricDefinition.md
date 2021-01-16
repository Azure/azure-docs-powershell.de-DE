---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
ms.openlocfilehash: 9ca873736ad86eaac17dd2795ad61716197ceaba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382652"
---
# <span data-ttu-id="6beb0-101">Get-AzMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="6beb0-101">Get-AzMetricDefinition</span></span>

## <span data-ttu-id="6beb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6beb0-102">SYNOPSIS</span></span>
<span data-ttu-id="6beb0-103">Ruft Metrikdefinitionen ab.</span><span class="sxs-lookup"><span data-stu-id="6beb0-103">Gets metric definitions.</span></span>

## <span data-ttu-id="6beb0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6beb0-104">SYNTAX</span></span>

```
Get-AzMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-MetricNamespace <String>]
 [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6beb0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6beb0-105">DESCRIPTION</span></span>
<span data-ttu-id="6beb0-106">Das **Cmdlet "Get-AzMetricDefinition"** ruft metrische Definitionen ab.</span><span class="sxs-lookup"><span data-stu-id="6beb0-106">The **Get-AzMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="6beb0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6beb0-107">EXAMPLES</span></span>

### <span data-ttu-id="6beb0-108">Beispiel 1: Erhalten von Metrikdefinitionen für eine Ressource</span><span class="sxs-lookup"><span data-stu-id="6beb0-108">Example 1: Get metric definitions for a resource</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2"
Name                   : CpuTime
Dimensions             : {}
MetricAvailabilities   : {Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability}
PrimaryAggregationType : Total
Properties             : {}
ResourceUri            : 
Unit                   : Seconds
Name                   : Requests
Dimensions             : {}
MetricAvailabilities   : {Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability}
PrimaryAggregationType : Total
Properties             : {}
ResourceUri            : 
Unit                   : Count
```

<span data-ttu-id="6beb0-109">Dieser Befehl ruft die Metrikdefinitionen für die angegebene Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="6beb0-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="6beb0-110">Beispiel 2: Erhalten von metrischen Definitionen mit detaillierter Ausgabe</span><span class="sxs-lookup"><span data-stu-id="6beb0-110">Example 2: Get metric definitions with detailed output</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : CpuTime
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Seconds
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : Requests
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Count
```

<span data-ttu-id="6beb0-111">Dieser Befehl ruft die metrischen Definitionen für "website2" ab.</span><span class="sxs-lookup"><span data-stu-id="6beb0-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="6beb0-112">Die Ausgabe wird detailliert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6beb0-112">The output is detailed.</span></span>

### <span data-ttu-id="6beb0-113">Beispiel 3: Erhalten von metrischen Definitionen nach Name</span><span class="sxs-lookup"><span data-stu-id="6beb0-113">Example 3: Get metric definitions by name</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput -MetricName "BytesSent,CpuTime"
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : CpuTime
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Seconds
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : BytesSent
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Bytes
```

<span data-ttu-id="6beb0-114">Dieser Befehl ruft Definitionen für die Metriken "BytesSent" und "CpuTime" ab.</span><span class="sxs-lookup"><span data-stu-id="6beb0-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="6beb0-115">Die Ausgabe wird detailliert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6beb0-115">The output is detailed.</span></span>

## <span data-ttu-id="6beb0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6beb0-116">PARAMETERS</span></span>

### <span data-ttu-id="6beb0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6beb0-117">-DefaultProfile</span></span>
<span data-ttu-id="6beb0-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6beb0-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6beb0-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="6beb0-119">-DetailedOutput</span></span>
<span data-ttu-id="6beb0-120">Gibt an, dass dieser Vorgang eine detaillierte Ausgabe enthielt.</span><span class="sxs-lookup"><span data-stu-id="6beb0-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="6beb0-121">Wenn Sie diesen Parameter nicht angeben, wird die Ausgabe zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="6beb0-121">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="6beb0-122">-MetricName</span><span class="sxs-lookup"><span data-stu-id="6beb0-122">-MetricName</span></span>
<span data-ttu-id="6beb0-123">Gibt ein Array von Namen von Metriken an.</span><span class="sxs-lookup"><span data-stu-id="6beb0-123">Specifies an array of names of metrics.</span></span>

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

### <span data-ttu-id="6beb0-124">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="6beb0-124">-MetricNamespace</span></span>
<span data-ttu-id="6beb0-125">Gibt den metrischen Namespace an, für den Metrikdefinitionen abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="6beb0-125">Specifies the metric namespace to query metric definitions for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6beb0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6beb0-126">-ResourceId</span></span>
<span data-ttu-id="6beb0-127">Gibt die Ressourcen-ID an.</span><span class="sxs-lookup"><span data-stu-id="6beb0-127">Specifies the resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6beb0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6beb0-128">CommonParameters</span></span>
<span data-ttu-id="6beb0-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6beb0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6beb0-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6beb0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6beb0-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6beb0-131">INPUTS</span></span>

### <span data-ttu-id="6beb0-132">System.String</span><span class="sxs-lookup"><span data-stu-id="6beb0-132">System.String</span></span>

### <span data-ttu-id="6beb0-133">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6beb0-133">System.String[]</span></span>

## <span data-ttu-id="6beb0-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6beb0-134">OUTPUTS</span></span>

### <span data-ttu-id="6beb0-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="6beb0-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span></span>

## <span data-ttu-id="6beb0-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6beb0-136">NOTES</span></span>

<span data-ttu-id="6beb0-137">Weitere Informationen zu den unterstützten Metriken finden Sie unter: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="6beb0-137">More information about the supported metrics may be found at: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="6beb0-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6beb0-138">RELATED LINKS</span></span>

<span data-ttu-id="6beb0-139">[Get-AzMetric](./Get-AzMetric.md) 
 [New-AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="6beb0-139">[Get-AzMetric](./Get-AzMetric.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>


