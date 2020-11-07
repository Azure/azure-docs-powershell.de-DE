---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetricdefinition
schema: 2.0.0
ms.openlocfilehash: 3f7edf37fbd7283f851b9641e41de5f39b96506b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848292"
---
# <span data-ttu-id="80292-101">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="80292-101">Get-AzureRmMetricDefinition</span></span>

## <span data-ttu-id="80292-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="80292-102">SYNOPSIS</span></span>
<span data-ttu-id="80292-103">Ruft metrische Definitionen ab.</span><span class="sxs-lookup"><span data-stu-id="80292-103">Gets metric definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80292-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="80292-104">SYNTAX</span></span>

```
Get-AzureRmMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-MetricNamespace <String>]
 [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80292-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80292-105">DESCRIPTION</span></span>
<span data-ttu-id="80292-106">Das Cmdlet " **Get-AzureRmMetricDefinition** " ruft metrische Definitionen ab.</span><span class="sxs-lookup"><span data-stu-id="80292-106">The **Get-AzureRmMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="80292-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="80292-107">EXAMPLES</span></span>

### <span data-ttu-id="80292-108">Beispiel 1: Abrufen von metrischen Definitionen für eine Ressource</span><span class="sxs-lookup"><span data-stu-id="80292-108">Example 1: Get metric definitions for a resource</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2"
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

<span data-ttu-id="80292-109">Dieser Befehl ruft die Metrik-Definitionen für die angegebene Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="80292-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="80292-110">Beispiel 2: Abrufen von metrischen Definitionen mit detaillierter Ausgabe</span><span class="sxs-lookup"><span data-stu-id="80292-110">Example 2: Get metric definitions with detailed output</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput
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

<span data-ttu-id="80292-111">Dieser Befehl ruft die metrischen Definitionen für website2 ab.</span><span class="sxs-lookup"><span data-stu-id="80292-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="80292-112">Die Ausgabe ist detailliert.</span><span class="sxs-lookup"><span data-stu-id="80292-112">The output is detailed.</span></span>

### <span data-ttu-id="80292-113">Beispiel 3: Abrufen von metrischen Definitionen nach Name</span><span class="sxs-lookup"><span data-stu-id="80292-113">Example 3: Get metric definitions by name</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput -MetricNames "BytesSent,CpuTime"
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

<span data-ttu-id="80292-114">Dieser Befehl ruft Definitionen für die BytesSent-und CpuTime-Metrik ab.</span><span class="sxs-lookup"><span data-stu-id="80292-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="80292-115">Die Ausgabe ist detailliert.</span><span class="sxs-lookup"><span data-stu-id="80292-115">The output is detailed.</span></span>

## <span data-ttu-id="80292-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="80292-116">PARAMETERS</span></span>

### <span data-ttu-id="80292-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80292-117">-DefaultProfile</span></span>
<span data-ttu-id="80292-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="80292-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80292-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="80292-119">-DetailedOutput</span></span>
<span data-ttu-id="80292-120">Gibt an, dass dieser Vorgang eine detaillierte Ausgabe enthielt.</span><span class="sxs-lookup"><span data-stu-id="80292-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="80292-121">Wenn Sie diesen Parameter nicht angeben, wird die Ausgabe zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="80292-121">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="80292-122">-Metricname</span><span class="sxs-lookup"><span data-stu-id="80292-122">-MetricName</span></span>
<span data-ttu-id="80292-123">Gibt ein Array mit Namen von Metriken an.</span><span class="sxs-lookup"><span data-stu-id="80292-123">Specifies an array of names of metrics.</span></span>

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

### <span data-ttu-id="80292-124">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="80292-124">-MetricNamespace</span></span>
<span data-ttu-id="80292-125">Gibt den metrischen Namespace an, für den metrische Definitionen abgefragt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="80292-125">Specifies the metric namespace to query metric definitions for.</span></span>

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

### <span data-ttu-id="80292-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="80292-126">-ResourceId</span></span>
<span data-ttu-id="80292-127">Gibt die Ressourcen-ID an.</span><span class="sxs-lookup"><span data-stu-id="80292-127">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="80292-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80292-128">CommonParameters</span></span>
<span data-ttu-id="80292-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80292-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80292-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80292-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80292-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="80292-131">INPUTS</span></span>

### <span data-ttu-id="80292-132">System. String</span><span class="sxs-lookup"><span data-stu-id="80292-132">System.String</span></span>

### <span data-ttu-id="80292-133">System. String []</span><span class="sxs-lookup"><span data-stu-id="80292-133">System.String[]</span></span>

## <span data-ttu-id="80292-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="80292-134">OUTPUTS</span></span>

### <span data-ttu-id="80292-135">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="80292-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span></span>

## <span data-ttu-id="80292-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="80292-136">NOTES</span></span>

## <span data-ttu-id="80292-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="80292-137">RELATED LINKS</span></span>

<span data-ttu-id="80292-138">[Get-AzureRmMetric](./Get-AzureRmMetric.md) 
 [Neu – AzureRmMetricFilter](./New-AzureRmMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="80292-138">[Get-AzureRmMetric](./Get-AzureRmMetric.md)
[New-AzureRmMetricFilter](./New-AzureRmMetricFilter.md)</span></span>


