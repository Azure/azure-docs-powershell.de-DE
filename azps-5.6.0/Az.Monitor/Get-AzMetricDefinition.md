---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
ms.openlocfilehash: 3e1038fc44acc1e3834ee10a1fd08bb49c35cd82
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932584"
---
# <span data-ttu-id="dbbd5-101">Get-AzMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="dbbd5-101">Get-AzMetricDefinition</span></span>

## <span data-ttu-id="dbbd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbbd5-102">SYNOPSIS</span></span>
<span data-ttu-id="dbbd5-103">Ruft Metrikdefinitionen ab.</span><span class="sxs-lookup"><span data-stu-id="dbbd5-103">Gets metric definitions.</span></span>

## <span data-ttu-id="dbbd5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dbbd5-104">SYNTAX</span></span>

```
Get-AzMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-MetricNamespace <String>]
 [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbbd5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dbbd5-105">DESCRIPTION</span></span>
<span data-ttu-id="dbbd5-106">Das **Get-AzMetricDefinition-Cmdlet** ruft Metrikdefinitionen ab.</span><span class="sxs-lookup"><span data-stu-id="dbbd5-106">The **Get-AzMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="dbbd5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dbbd5-107">EXAMPLES</span></span>

### <span data-ttu-id="dbbd5-108">Beispiel 1: Metrikdefinitionen für eine Ressource erhalten</span><span class="sxs-lookup"><span data-stu-id="dbbd5-108">Example 1: Get metric definitions for a resource</span></span>
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

<span data-ttu-id="dbbd5-109">Dieser Befehl ruft die Metrikdefinitionen für die angegebene Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="dbbd5-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="dbbd5-110">Beispiel 2: Erhalten von Metrikdefinitionen mit detaillierter Ausgabe</span><span class="sxs-lookup"><span data-stu-id="dbbd5-110">Example 2: Get metric definitions with detailed output</span></span>
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

<span data-ttu-id="dbbd5-111">Dieser Befehl ruft die Metrikdefinitionen für website2 ab.</span><span class="sxs-lookup"><span data-stu-id="dbbd5-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="dbbd5-112">Die Ausgabe ist detailliert.</span><span class="sxs-lookup"><span data-stu-id="dbbd5-112">The output is detailed.</span></span>

### <span data-ttu-id="dbbd5-113">Beispiel 3: Erhalten von Metrikdefinitionen nach Name</span><span class="sxs-lookup"><span data-stu-id="dbbd5-113">Example 3: Get metric definitions by name</span></span>
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

<span data-ttu-id="dbbd5-114">Dieser Befehl ruft Definitionen für die BytesSent- und CpuTime-Metriken ab.</span><span class="sxs-lookup"><span data-stu-id="dbbd5-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="dbbd5-115">Die Ausgabe ist detailliert.</span><span class="sxs-lookup"><span data-stu-id="dbbd5-115">The output is detailed.</span></span>

## <span data-ttu-id="dbbd5-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dbbd5-116">PARAMETERS</span></span>

### <span data-ttu-id="dbbd5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbbd5-117">-DefaultProfile</span></span>
<span data-ttu-id="dbbd5-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="dbbd5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbbd5-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="dbbd5-119">-DetailedOutput</span></span>
<span data-ttu-id="dbbd5-120">Gibt an, dass dieser Vorgang eine detaillierte Ausgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="dbbd5-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="dbbd5-121">Wenn Sie diesen Parameter nicht angeben, wird die Ausgabe zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="dbbd5-121">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="dbbd5-122">-MetricName</span><span class="sxs-lookup"><span data-stu-id="dbbd5-122">-MetricName</span></span>
<span data-ttu-id="dbbd5-123">Gibt ein Array mit Namen von Metriken an.</span><span class="sxs-lookup"><span data-stu-id="dbbd5-123">Specifies an array of names of metrics.</span></span>

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

### <span data-ttu-id="dbbd5-124">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="dbbd5-124">-MetricNamespace</span></span>
<span data-ttu-id="dbbd5-125">Gibt den Metriknamespace an, für den Metrikdefinitionen abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="dbbd5-125">Specifies the metric namespace to query metric definitions for.</span></span>

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

### <span data-ttu-id="dbbd5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dbbd5-126">-ResourceId</span></span>
<span data-ttu-id="dbbd5-127">Gibt die Ressourcen-ID an.</span><span class="sxs-lookup"><span data-stu-id="dbbd5-127">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="dbbd5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbbd5-128">CommonParameters</span></span>
<span data-ttu-id="dbbd5-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbbd5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbbd5-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dbbd5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbbd5-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dbbd5-131">INPUTS</span></span>

### <span data-ttu-id="dbbd5-132">System.String</span><span class="sxs-lookup"><span data-stu-id="dbbd5-132">System.String</span></span>

### <span data-ttu-id="dbbd5-133">System.String[]</span><span class="sxs-lookup"><span data-stu-id="dbbd5-133">System.String[]</span></span>

## <span data-ttu-id="dbbd5-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dbbd5-134">OUTPUTS</span></span>

### <span data-ttu-id="dbbd5-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="dbbd5-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span></span>

## <span data-ttu-id="dbbd5-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="dbbd5-136">NOTES</span></span>

<span data-ttu-id="dbbd5-137">Weitere Informationen zu den unterstützten Metriken finden Sie unter: https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="dbbd5-137">More information about the supported metrics may be found at: https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="dbbd5-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="dbbd5-138">RELATED LINKS</span></span>

<span data-ttu-id="dbbd5-139">[Get-AzMetric](./Get-AzMetric.md) 
 [New-AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="dbbd5-139">[Get-AzMetric](./Get-AzMetric.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>


