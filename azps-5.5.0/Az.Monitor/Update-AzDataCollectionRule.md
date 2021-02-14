---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzDataCollectionRule.md
ms.openlocfilehash: a655ac87dcc99eca1a8c5a5329d2073d54614ceb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157297"
---
# <span data-ttu-id="066fb-101">Update-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="066fb-101">Update-AzDataCollectionRule</span></span>

## <span data-ttu-id="066fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="066fb-102">SYNOPSIS</span></span>
<span data-ttu-id="066fb-103">Aktualisiert eine Eigenschaft für Datensammlungsregeltags.</span><span class="sxs-lookup"><span data-stu-id="066fb-103">Updates a data collection rule tags property.</span></span>

## <span data-ttu-id="066fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="066fb-104">SYNTAX</span></span>

### <span data-ttu-id="066fb-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="066fb-105">ByName (Default)</span></span>
```
Update-AzDataCollectionRule 
      -ResourceGroupName <string> 
      -RuleName <string> 
      [-Tag <hashtable>] 
      [-DefaultProfile <IAzureContextContainer>] 
      [-WhatIf] 
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="066fb-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="066fb-106">ByResourceId</span></span>
```
Update-AzDataCollectionRule 
      -RuleId <string> 
      [-Tag <hashtable>] 
      [-DefaultProfile <IAzureContextContainer>] 
      [-WhatIf] 
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="066fb-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="066fb-107">ByInputObject</span></span>
```
Update-AzDataCollectionRule 
      -InputObject <PSDataCollectionRuleResource> 
      [-Tag <hashtable>] 
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

## <span data-ttu-id="066fb-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="066fb-108">DESCRIPTION</span></span>
<span data-ttu-id="066fb-109">Das **Cmdlet "Update-AzDataCollectionRule"** aktualisiert die Eigenschaft "Tags" für Datensammlungsregel.</span><span class="sxs-lookup"><span data-stu-id="066fb-109">The **Update-AzDataCollectionRule** cmdlet updates a data collection rule Tags property.</span></span>

<span data-ttu-id="066fb-110">Datensammlungsregeln (Data Collection Rules, DCR) definieren Daten, die in Azure Monitor übermittelt werden, und geben an, wohin diese Daten gesendet oder gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="066fb-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="066fb-111">Hier finden Sie den vollständigen [DcR-Übersichtsartikel.](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="066fb-111">Here is the complete [DCR overview article](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="066fb-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="066fb-112">EXAMPLES</span></span>

### <span data-ttu-id="066fb-113">Beispiel 1: Aktualisieren von Datensammlungsregeltags</span><span class="sxs-lookup"><span data-stu-id="066fb-113">Example 1: Update data collection rule tags</span></span>
```
PS C:\>Update-AzDataCollectionRule -RuleName 'newDcr'
                                   -ResourceGroupName 'testdcr'
                                   -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : 
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr
Name              : newDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="066fb-114">Mit diesem Befehl wird die Tageigenschaft für die angegebene Datensammlungsregel aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="066fb-114">This command updates the tags property for the given data collection rule.</span></span>

### <span data-ttu-id="066fb-115">Beispiel 2: Aktualisieren von Datensammlungsregeltags</span><span class="sxs-lookup"><span data-stu-id="066fb-115">Example 2: Update data collection rule tags</span></span>
```
PS C:\>Update-AzDataCollectionRule -RuleId '/subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr'
                                   -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : 
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr
Name              : newDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="066fb-116">Mit diesem Befehl wird die Tageigenschaft für die angegebene Datensammlungsregel aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="066fb-116">This command updates the tags property for the given data collection rule.</span></span>

### <span data-ttu-id="066fb-117">Beispiel 3: Aktualisieren von Datensammlungsregeltags</span><span class="sxs-lookup"><span data-stu-id="066fb-117">Example 3: Update data collection rule tags</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName "testdcr" -Name "newDcr"
PS C:\>$dcr | Update-AzDataCollectionRule -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : 
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : {provState}
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr
Name              : newDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="066fb-118">Mit diesem Befehl wird die Tageigenschaft für die angegebene Datensammlungsregel aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="066fb-118">This command updates the tags property for the given data collection rule.</span></span>

## <span data-ttu-id="066fb-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="066fb-119">PARAMETERS</span></span>

### <span data-ttu-id="066fb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="066fb-120">-DefaultProfile</span></span>
<span data-ttu-id="066fb-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="066fb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="066fb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="066fb-122">-ResourceGroupName</span></span>
<span data-ttu-id="066fb-123">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="066fb-123">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="066fb-124">-RuleName</span><span class="sxs-lookup"><span data-stu-id="066fb-124">-RuleName</span></span>
<span data-ttu-id="066fb-125">Der Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="066fb-125">The resource name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="066fb-126">-RuleId</span><span class="sxs-lookup"><span data-stu-id="066fb-126">-RuleId</span></span>
<span data-ttu-id="066fb-127">Die Ressourcen-ID der Datensammlungsregel</span><span class="sxs-lookup"><span data-stu-id="066fb-127">The resource ID of the data collection rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="066fb-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="066fb-128">-InputObject</span></span>
<span data-ttu-id="066fb-129">PSDataCollectionRuleResource-Objekt</span><span class="sxs-lookup"><span data-stu-id="066fb-129">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="066fb-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="066fb-130">-Tag</span></span>
<span data-ttu-id="066fb-131">Die Tageigenschaft der Datensammlungsregel</span><span class="sxs-lookup"><span data-stu-id="066fb-131">The tags property of the data collection rule</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: Falose
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="066fb-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="066fb-132">-Confirm</span></span>
<span data-ttu-id="066fb-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="066fb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="066fb-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="066fb-134">-WhatIf</span></span>
<span data-ttu-id="066fb-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="066fb-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="066fb-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="066fb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="066fb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="066fb-137">CommonParameters</span></span>
<span data-ttu-id="066fb-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="066fb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="066fb-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="066fb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="066fb-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="066fb-140">INPUTS</span></span>

### <span data-ttu-id="066fb-141">System.String</span><span class="sxs-lookup"><span data-stu-id="066fb-141">System.String</span></span>

## <span data-ttu-id="066fb-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="066fb-142">OUTPUTS</span></span>

### <span data-ttu-id="066fb-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="066fb-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="066fb-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="066fb-144">NOTES</span></span>

## <span data-ttu-id="066fb-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="066fb-145">RELATED LINKS</span></span>

<span data-ttu-id="066fb-146">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="066fb-146">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)</span></span>