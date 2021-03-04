---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A70F4C03-E842-45D5-9323-DC5B14B569F1
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azautoscalehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAutoscaleHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAutoscaleHistory.md
ms.openlocfilehash: c88cd3bbf132ccb7b8913b15dcc66f58ea2d2db3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932667"
---
# <span data-ttu-id="6b22e-101">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="6b22e-101">Get-AzAutoscaleHistory</span></span>

## <span data-ttu-id="6b22e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b22e-102">SYNOPSIS</span></span>
<span data-ttu-id="6b22e-103">Ruft den Verlauf der automatischen Skalierung ab.</span><span class="sxs-lookup"><span data-stu-id="6b22e-103">Gets the Autoscale history.</span></span>

## <span data-ttu-id="6b22e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b22e-104">SYNTAX</span></span>

```
Get-AzAutoscaleHistory [-ResourceId <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>]
 [-Caller <String>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b22e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b22e-105">DESCRIPTION</span></span>
<span data-ttu-id="6b22e-106">Das **Get-AzAutoscaleHistory-Cmdlet** ruft den Verlauf von Ereignissen ab, die mit einer Einstellung für die automatische Skalierung verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="6b22e-106">The **Get-AzAutoscaleHistory** cmdlet gets the history of events related to an Autoscale setting.</span></span>

## <span data-ttu-id="6b22e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6b22e-107">EXAMPLES</span></span>

### <span data-ttu-id="6b22e-108">Beispiel 1: Alle ereignisse, die einem Abonnement zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="6b22e-108">Example 1: Get all events associated with a subscription</span></span>
```
PS C:\>Get-AzAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -DetailedOutput
```

<span data-ttu-id="6b22e-109">Dieser Befehl ruft alle autoscalebezogenen Ereignisse ab, die dem aktuellen Abonnement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6b22e-109">This command gets all of the Autoscale-related events associated with the current subscription.</span></span>

### <span data-ttu-id="6b22e-110">Beispiel 2: GetAutoscaleHistory für eine bestimmte Ressource</span><span class="sxs-lookup"><span data-stu-id="6b22e-110">Example 2: GetAutoscaleHistory for a particular resource</span></span>
```
PS C:\>Get-AzAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -ResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS" -DetailedOutput
Authorization        : 
Caller               : Microsoft.Insights/autoscaleSettings
Claims               :  http://schemas.xmlsoap.org/ws/2005/05/identity/claims/spn: Microsoft.Insights/autoscaleSettings
CorrelationId        : ac5b03ca-05d4-4811-9c27-0314a145f785
Description          : The autoscale engine attempting to scale resource '/subscriptions/a93fb07c-6c93-40be-bf3b-4f0deb
                       a10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm'
                       from 1 instances count to 2 instances count. 
EventDataId          : c554f7ed-514c-449c-9338-13e15b4b56a3
EventName            : AutoscaleAction
EventSource          : microsoft.insights/autoscalesettings
EventTimestamp       : 2/10/2015 2:38:19 AM
HttpRequest          : 
Id                   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS/events/c554f7ed-514c-4
                       49c-9338-13e15b4b56a3/ticks/635591326997519815
Level                : Informational
OperationId          : ac5b03ca-05d4-4811-9c27-0314a145f785
OperationName        : ScaleUp
Properties           : 
Description    : The autoscale engine attempting to scale resource '/subscriptions/a93fb07c-6c93
                       -40be-bf3b-4f0deba10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/De
                       faultServerFarm' from 1 instances count to 2 instances count. 
ResourceName   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-
                       EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
OldInstancesCount: 1
NewInstancesCount: 2
ActiveAutoscaleProfile: {
                         "Name": "No scheduled times",
                         "Capacity": {
                           "Minimum": "1",
                           "Maximum": "3",
                           "Default": "1"
                         },
                         "Rules": [
                           {
                             "MetricTrigger": {
                               "Name": "CpuPercentage",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT45M",
                               "TimeAggregation": "Average",
                               "Operator": "GreaterThanOrEqual",
                               "Threshold": 14.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Increase",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT5M"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "CpuPercentage",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT45M",
                               "TimeAggregation": "Average",
                               "Operator": "LessThanOrEqual",
                               "Threshold": 4.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Decrease",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT2H"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "BytesReceived",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT10M",
                               "TimeAggregation": "Average",
                               "Operator": "LessThanOrEqual",
                               "Threshold": 50.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Decrease",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT10M"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "BytesReceived",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT5M",
                               "TimeAggregation": "Average",
                               "Operator": "GreaterThanOrEqual",
                               "Threshold": 100.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Increase",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT10M"
                             }
                           }
                         ] 
                       }
ResourceGroupName    : Default-Web-EastUS
ResourceProviderName : microsoft.insights
ResourceId           : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS
Status               : Succeeded
SubmissionTimestamp  : 2/10/2015 2:38:19 AM
SubscriptionId       : b93fb07a-6f93-30be-bf3e-4f0deca15f4f
SubStatus            :
```

<span data-ttu-id="6b22e-111">Dieser Befehl ruft alle mit der Automatischen Skalierung zusammenhängenden Ereignisse ab, die einer bestimmten Ressource zugeordnet sind, die durch die RESSOURCEN-ID (im Wesentlichen den ResourceUri) identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="6b22e-111">This command gets all Autoscale-related events associated with a particular resource identified by the resource's ID (essentially, the ResourceUri).</span></span>

## <span data-ttu-id="6b22e-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6b22e-112">PARAMETERS</span></span>

### <span data-ttu-id="6b22e-113">-Anrufer</span><span class="sxs-lookup"><span data-stu-id="6b22e-113">-Caller</span></span>
<span data-ttu-id="6b22e-114">Gibt einen Anrufer an.</span><span class="sxs-lookup"><span data-stu-id="6b22e-114">Specifies a caller.</span></span>

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

### <span data-ttu-id="6b22e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b22e-115">-DefaultProfile</span></span>
<span data-ttu-id="6b22e-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6b22e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b22e-117">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="6b22e-117">-DetailedOutput</span></span>
<span data-ttu-id="6b22e-118">Gibt an, dass dieser Vorgang eine detaillierte Ausgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="6b22e-118">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="6b22e-119">Wenn Sie diesen Parameter nicht angeben, wird die Ausgabe zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="6b22e-119">If you do not specify this parameter, the output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b22e-120">-EndTime</span><span class="sxs-lookup"><span data-stu-id="6b22e-120">-EndTime</span></span>
<span data-ttu-id="6b22e-121">Gibt die Endzeit der Abfrage in der lokalen Zeit an.</span><span class="sxs-lookup"><span data-stu-id="6b22e-121">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="6b22e-122">Die Standardeinstellung ist die aktuelle Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="6b22e-122">The default is the current time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b22e-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b22e-123">-ResourceId</span></span>
<span data-ttu-id="6b22e-124">Gibt die Ressourcen-ID an, der die Einstellung für die automatische Skalierung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6b22e-124">Specifies the resource ID to which the autoscale setting is associated.</span></span>

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

### <span data-ttu-id="6b22e-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6b22e-125">-StartTime</span></span>
<span data-ttu-id="6b22e-126">Gibt die Startzeit der Abfrage in der lokalen Zeit an.</span><span class="sxs-lookup"><span data-stu-id="6b22e-126">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="6b22e-127">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6b22e-127">This parameter is optional.</span></span>
<span data-ttu-id="6b22e-128">Die Standardeinstellung ist die aktuelle Ortszeit minus eine Stunde.</span><span class="sxs-lookup"><span data-stu-id="6b22e-128">The default is the current local time minus one hour.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b22e-129">-Status</span><span class="sxs-lookup"><span data-stu-id="6b22e-129">-Status</span></span>
<span data-ttu-id="6b22e-130">Gibt einen Filter nach Status an.</span><span class="sxs-lookup"><span data-stu-id="6b22e-130">Specifies a filter by status.</span></span>
<span data-ttu-id="6b22e-131">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6b22e-131">This parameter is optional.</span></span>
<span data-ttu-id="6b22e-132">Der Fehler ist eine leere Zeichenfolge (d. h. kein Filter)</span><span class="sxs-lookup"><span data-stu-id="6b22e-132">The fault is an empty string (i.e. no filter)</span></span>

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

### <span data-ttu-id="6b22e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b22e-133">CommonParameters</span></span>
<span data-ttu-id="6b22e-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b22e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b22e-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b22e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b22e-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6b22e-136">INPUTS</span></span>

### <span data-ttu-id="6b22e-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6b22e-137">System.String</span></span>

### <span data-ttu-id="6b22e-138">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6b22e-138">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6b22e-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6b22e-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6b22e-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6b22e-140">OUTPUTS</span></span>

### <span data-ttu-id="6b22e-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span><span class="sxs-lookup"><span data-stu-id="6b22e-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="6b22e-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6b22e-142">NOTES</span></span>

## <span data-ttu-id="6b22e-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6b22e-143">RELATED LINKS</span></span>

[<span data-ttu-id="6b22e-144">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="6b22e-144">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="6b22e-145">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="6b22e-145">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="6b22e-146">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="6b22e-146">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


