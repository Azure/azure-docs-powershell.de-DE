---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRule.md
ms.openlocfilehash: cdde294c3af4684146d265e2024f6948660312bb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170225"
---
# <span data-ttu-id="093c3-101">New-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="093c3-101">New-AzDataCollectionRule</span></span>

## <span data-ttu-id="093c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="093c3-102">SYNOPSIS</span></span>
<span data-ttu-id="093c3-103">Erstellen Sie eine Datensammlungsregel.</span><span class="sxs-lookup"><span data-stu-id="093c3-103">Create a data collection rule.</span></span>

## <span data-ttu-id="093c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="093c3-104">SYNTAX</span></span>

### <span data-ttu-id="093c3-105">ByFile (Standard)</span><span class="sxs-lookup"><span data-stu-id="093c3-105">ByFile (Default)</span></span>
```
New-AzDataCollectionRule
   -Location <string>
   -ResourceGroupName <string>
   -RuleName <string>
   -RuleFile <string>
   [-Description <string>]
   [-Tag <hashtable>]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="093c3-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="093c3-106">DESCRIPTION</span></span>
<span data-ttu-id="093c3-107">Das **Cmdlet "New-AzDataCollectionRule"** erstellt eine Datensammlungsregel.</span><span class="sxs-lookup"><span data-stu-id="093c3-107">The **New-AzDataCollectionRule** cmdlet creates a data collection rule.</span></span>

<span data-ttu-id="093c3-108">Datensammlungsregeln (Data Collection Rules, DCR) definieren Daten, die in Azure Monitor übermittelt werden, und geben an, wohin diese Daten gesendet oder gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="093c3-108">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="093c3-109">Hier finden Sie den vollständigen [DcR-Übersichtsartikel.](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="093c3-109">Here is the complete [DCR overview article](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

<span data-ttu-id="093c3-110">Um den Parameter "-RuleFile" zu verwenden, erstellen Sie eine json-Datei, die drei Eigenschaften enthält: Datenquellen, Ziele, Datenflüsse (siehe Beispiel #1)</span><span class="sxs-lookup"><span data-stu-id="093c3-110">To use the -RuleFile parameter, construct a json file containing three properties: dataSources, destinations, dataFlows (see Example #1)</span></span>

<span data-ttu-id="093c3-111">Die Schemadetails finden Sie [hier.](https://docs.microsoft.com/en-us/rest/api/monitor/datacollectionrules/create)</span><span class="sxs-lookup"><span data-stu-id="093c3-111">You may find here the [schema detail](https://docs.microsoft.com/en-us/rest/api/monitor/datacollectionrules/create).</span></span>

<span data-ttu-id="093c3-112">Die Ausgabe eines DCR, der mit dem Cmdlet ConvertTo-Json serialisiert wurde, wird ebenfalls unterstützt (siehe Beispiel #2).</span><span class="sxs-lookup"><span data-stu-id="093c3-112">The output of a DCR serialized with the cmdlet ConvertTo-Json is also supported (see Example #2).</span></span>

## <span data-ttu-id="093c3-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="093c3-113">EXAMPLES</span></span>

### <span data-ttu-id="093c3-114">Beispiel 1: Erstellen einer Datensammlungsregel, JSON aus Rest API</span><span class="sxs-lookup"><span data-stu-id="093c3-114">Example 1: Create data collection rule, JSON from Rest API</span></span>
```powershell
PS C:\>New-AzDataCollectionRule -Location 'East US 2 EUAP' -ResourceGroupName 'testdcr'
                                -RuleName 'newDcrEx1' -RuleFile 'C:\samples\dcrEx1.json'
                                -Description 'Dcr description'
                                -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : Dcr description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcrEx1
Name              : newDcrEx1
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcrEx1.json
{
  "properties": {
    "dataSources": {
      "performanceCounters": [
        {
          "streams": [
            "Microsoft-InsightsMetrics"
          ],
          "scheduledTransferPeriod": "PT1M",
          "samplingFrequencyInSeconds": 10,
          "counterSpecifiers": [
            "\\Processor Information(_Total)\\% Processor Time"
          ],
          "name": "perfCounter01"
        }
      ]
    },
    "destinations": {
      "azureMonitorMetrics": {
        "name": "azureMonitorMetrics-default"
      }
    },
    "dataFlows": [
      {
        "streams": [
          "Microsoft-InsightsMetrics"
        ],
        "destinations": [
          "azureMonitorMetrics-default"
        ]
      }
    ]
  }
}
```

<span data-ttu-id="093c3-115">Mit diesem Befehl werden Datensammlungsregeln für das aktuelle Abonnement erstellt.</span><span class="sxs-lookup"><span data-stu-id="093c3-115">This command creates a data collection rules for the current subscription.</span></span>

### <span data-ttu-id="093c3-116">Beispiel 2: Erstellen einer Datensammlungsregel, JSON aus PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="093c3-116">Example 2: Create data collection rule, JSON from PSDataCollectionRuleResource</span></span>
```powershell
PS C:\>New-AzDataCollectionRule -Location 'East US 2 EUAP' -ResourceGroupName 'testdcr'
                                -RuleName 'newDcrEx2' -RuleFile 'C:\samples\dcrEx2.json'
                                -Description 'Dcr description'
                                -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : Dcr description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcrEx2
Name              : newDcrEx2
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcrEx2.json
{
  "DataSources": {
    "PerformanceCounters": [
      {
        "Streams": [
          "Microsoft-InsightsMetrics"
        ],
        "ScheduledTransferPeriod": "PT1M",
        "SamplingFrequencyInSeconds": 10,
        "CounterSpecifiers": [
          "\\Processor Information(_Total)\\% Processor Time"
        ],
        "Name": "perfCounter01"
      }
    ]
  },
  "Destinations": {
    "AzureMonitorMetrics": {
      "Name": "azureMonitorMetrics-default"
    }
  },
  "DataFlows": [
    {
      "Streams": [
        "Microsoft-InsightsMetrics"
      ],
      "Destinations": [
        "azureMonitorMetrics-default"
      ]
    }
  ]
}
```

<span data-ttu-id="093c3-117">Mit diesem Befehl werden Datensammlungsregeln für das aktuelle Abonnement erstellt.</span><span class="sxs-lookup"><span data-stu-id="093c3-117">This command creates a data collection rules for the current subscription.</span></span>

## <span data-ttu-id="093c3-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="093c3-118">PARAMETERS</span></span>

### <span data-ttu-id="093c3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="093c3-119">-DefaultProfile</span></span>
<span data-ttu-id="093c3-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="093c3-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="093c3-121">-Location</span><span class="sxs-lookup"><span data-stu-id="093c3-121">-Location</span></span>
<span data-ttu-id="093c3-122">Ressourcenspeicherort</span><span class="sxs-lookup"><span data-stu-id="093c3-122">The resource location</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="093c3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="093c3-123">-ResourceGroupName</span></span>
<span data-ttu-id="093c3-124">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="093c3-124">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="093c3-125">-RuleName</span><span class="sxs-lookup"><span data-stu-id="093c3-125">-RuleName</span></span>
<span data-ttu-id="093c3-126">Der Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="093c3-126">The resource name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="093c3-127">-RuleFile</span><span class="sxs-lookup"><span data-stu-id="093c3-127">-RuleFile</span></span>
<span data-ttu-id="093c3-128">Der Dateipfad von JSON</span><span class="sxs-lookup"><span data-stu-id="093c3-128">The JSON file path</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="093c3-129">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="093c3-129">-Description</span></span>
<span data-ttu-id="093c3-130">Ressourcenbeschreibung</span><span class="sxs-lookup"><span data-stu-id="093c3-130">The resource description</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="093c3-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="093c3-131">-Tag</span></span>
<span data-ttu-id="093c3-132">Die Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="093c3-132">The resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="093c3-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="093c3-133">-Confirm</span></span>
<span data-ttu-id="093c3-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="093c3-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="093c3-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="093c3-135">-WhatIf</span></span>
<span data-ttu-id="093c3-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="093c3-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="093c3-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="093c3-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="093c3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="093c3-138">CommonParameters</span></span>
<span data-ttu-id="093c3-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="093c3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="093c3-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="093c3-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="093c3-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="093c3-141">INPUTS</span></span>

### <span data-ttu-id="093c3-142">System.String</span><span class="sxs-lookup"><span data-stu-id="093c3-142">System.String</span></span>

## <span data-ttu-id="093c3-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="093c3-143">OUTPUTS</span></span>

### <span data-ttu-id="093c3-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="093c3-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="093c3-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="093c3-145">NOTES</span></span>

## <span data-ttu-id="093c3-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="093c3-146">RELATED LINKS</span></span>

<span data-ttu-id="093c3-147">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="093c3-147">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>