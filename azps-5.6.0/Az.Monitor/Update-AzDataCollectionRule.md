---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/update-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzDataCollectionRule.md
ms.openlocfilehash: 2e4aba9a2572b5612070d860dcbe20cda2366a02
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940376"
---
# <span data-ttu-id="7bf74-101">Update-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="7bf74-101">Update-AzDataCollectionRule</span></span>

## <span data-ttu-id="7bf74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bf74-102">SYNOPSIS</span></span>
<span data-ttu-id="7bf74-103">Aktualisiert eine Eigenschaft für Datensammlungsregeltags.</span><span class="sxs-lookup"><span data-stu-id="7bf74-103">Updates a data collection rule tags property.</span></span>

## <span data-ttu-id="7bf74-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7bf74-104">SYNTAX</span></span>

### <span data-ttu-id="7bf74-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7bf74-105">ByName (Default)</span></span>
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

### <span data-ttu-id="7bf74-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7bf74-106">ByResourceId</span></span>
```
Update-AzDataCollectionRule 
      -RuleId <string> 
      [-Tag <hashtable>] 
      [-DefaultProfile <IAzureContextContainer>] 
      [-WhatIf] 
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="7bf74-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7bf74-107">ByInputObject</span></span>
```
Update-AzDataCollectionRule 
      -InputObject <PSDataCollectionRuleResource> 
      [-Tag <hashtable>] 
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

## <span data-ttu-id="7bf74-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7bf74-108">DESCRIPTION</span></span>
<span data-ttu-id="7bf74-109">Das **Cmdlet Update-AzDataCollectionRule** aktualisiert eine Eigenschaft für Datensammlungsregeltags.</span><span class="sxs-lookup"><span data-stu-id="7bf74-109">The **Update-AzDataCollectionRule** cmdlet updates a data collection rule Tags property.</span></span>

<span data-ttu-id="7bf74-110">Datensammlungsregeln (Data Collection Rules, DCR) definieren Daten, die in Azure Monitor übermittelt werden, und geben an, wo diese Daten gesendet oder gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7bf74-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="7bf74-111">Hier finden Sie den vollständigen [DCR-Übersichtsartikel](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span><span class="sxs-lookup"><span data-stu-id="7bf74-111">Here is the complete [DCR overview article](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="7bf74-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7bf74-112">EXAMPLES</span></span>

### <span data-ttu-id="7bf74-113">Beispiel 1: Aktualisieren von Datensammlungsregeltags</span><span class="sxs-lookup"><span data-stu-id="7bf74-113">Example 1: Update data collection rule tags</span></span>
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

<span data-ttu-id="7bf74-114">Mit diesem Befehl wird die -Tags-Eigenschaft für die angegebene Datensammlungsregel aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7bf74-114">This command updates the tags property for the given data collection rule.</span></span>

### <span data-ttu-id="7bf74-115">Beispiel 2: Aktualisieren von Datensammlungsregeltags</span><span class="sxs-lookup"><span data-stu-id="7bf74-115">Example 2: Update data collection rule tags</span></span>
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

<span data-ttu-id="7bf74-116">Mit diesem Befehl wird die -Tags-Eigenschaft für die angegebene Datensammlungsregel aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7bf74-116">This command updates the tags property for the given data collection rule.</span></span>

### <span data-ttu-id="7bf74-117">Beispiel 3: Aktualisieren von Datensammlungsregeltags</span><span class="sxs-lookup"><span data-stu-id="7bf74-117">Example 3: Update data collection rule tags</span></span>
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

<span data-ttu-id="7bf74-118">Mit diesem Befehl wird die -Tags-Eigenschaft für die angegebene Datensammlungsregel aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7bf74-118">This command updates the tags property for the given data collection rule.</span></span>

## <span data-ttu-id="7bf74-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7bf74-119">PARAMETERS</span></span>

### <span data-ttu-id="7bf74-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bf74-120">-DefaultProfile</span></span>
<span data-ttu-id="7bf74-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7bf74-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7bf74-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bf74-122">-ResourceGroupName</span></span>
<span data-ttu-id="7bf74-123">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="7bf74-123">The resource group name</span></span>

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

### <span data-ttu-id="7bf74-124">-RuleName</span><span class="sxs-lookup"><span data-stu-id="7bf74-124">-RuleName</span></span>
<span data-ttu-id="7bf74-125">Der Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="7bf74-125">The resource name</span></span>

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

### <span data-ttu-id="7bf74-126">-RuleId</span><span class="sxs-lookup"><span data-stu-id="7bf74-126">-RuleId</span></span>
<span data-ttu-id="7bf74-127">Die Ressourcen-ID der Datensammlungsregel</span><span class="sxs-lookup"><span data-stu-id="7bf74-127">The resource ID of the data collection rule</span></span>

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

### <span data-ttu-id="7bf74-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7bf74-128">-InputObject</span></span>
<span data-ttu-id="7bf74-129">PSDataCollectionRuleResource-Objekt</span><span class="sxs-lookup"><span data-stu-id="7bf74-129">PSDataCollectionRuleResource Object</span></span>

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

### <span data-ttu-id="7bf74-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="7bf74-130">-Tag</span></span>
<span data-ttu-id="7bf74-131">Die Tags-Eigenschaft der Datensammlungsregel</span><span class="sxs-lookup"><span data-stu-id="7bf74-131">The tags property of the data collection rule</span></span>

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

### <span data-ttu-id="7bf74-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7bf74-132">-Confirm</span></span>
<span data-ttu-id="7bf74-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7bf74-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bf74-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bf74-134">-WhatIf</span></span>
<span data-ttu-id="7bf74-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7bf74-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7bf74-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7bf74-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bf74-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bf74-137">CommonParameters</span></span>
<span data-ttu-id="7bf74-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bf74-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bf74-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7bf74-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bf74-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7bf74-140">INPUTS</span></span>

### <span data-ttu-id="7bf74-141">System.String</span><span class="sxs-lookup"><span data-stu-id="7bf74-141">System.String</span></span>

## <span data-ttu-id="7bf74-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7bf74-142">OUTPUTS</span></span>

### <span data-ttu-id="7bf74-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="7bf74-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="7bf74-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7bf74-144">NOTES</span></span>

## <span data-ttu-id="7bf74-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7bf74-145">RELATED LINKS</span></span>

<span data-ttu-id="7bf74-146">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="7bf74-146">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)</span></span>