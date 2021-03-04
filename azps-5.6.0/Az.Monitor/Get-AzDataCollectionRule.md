---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRule.md
ms.openlocfilehash: 6c1ea4cd7abbf50fb00a5f7fe1b04b7112b8f6c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932659"
---
# <span data-ttu-id="0161d-101">Get-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="0161d-101">Get-AzDataCollectionRule</span></span>

## <span data-ttu-id="0161d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0161d-102">SYNOPSIS</span></span>
<span data-ttu-id="0161d-103">Ruft Datensammlungsregel(en) ab.</span><span class="sxs-lookup"><span data-stu-id="0161d-103">Gets data collection rule(s).</span></span>

## <span data-ttu-id="0161d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0161d-104">SYNTAX</span></span>

### <span data-ttu-id="0161d-105">BySubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="0161d-105">BySubscription (Default)</span></span>
```
Get-AzDataCollectionRule
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="0161d-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0161d-106">ByResourceGroup</span></span>
```
Get-AzDataCollectionRule
   -ResourceGroupName <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="0161d-107">ByName</span><span class="sxs-lookup"><span data-stu-id="0161d-107">ByName</span></span>
```
Get-AzDataCollectionRule
   -ResourceGroupName <string>
   -RuleName <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="0161d-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0161d-108">ByResourceId</span></span>
```
Get-AzDataCollectionRule
   -RuleId <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

## <span data-ttu-id="0161d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0161d-109">DESCRIPTION</span></span>
<span data-ttu-id="0161d-110">Das **Get-AzDataCollectionRule-Cmdlet** ruft mindestens eine Datensammlungsregeln ab.</span><span class="sxs-lookup"><span data-stu-id="0161d-110">The **Get-AzDataCollectionRule** cmdlet gets one or more data collection rules.</span></span>

<span data-ttu-id="0161d-111">Datensammlungsregeln (Data Collection Rules, DCR) definieren Daten, die in Azure Monitor übermittelt werden, und geben an, wo diese Daten gesendet oder gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0161d-111">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="0161d-112">Hier finden Sie den vollständigen [DCR-Übersichtsartikel](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span><span class="sxs-lookup"><span data-stu-id="0161d-112">Here is the complete [DCR overview article](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="0161d-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0161d-113">EXAMPLES</span></span>

### <span data-ttu-id="0161d-114">Beispiel 1: Datensammlungsregeln nach Abonnement-ID erhalten</span><span class="sxs-lookup"><span data-stu-id="0161d-114">Example 1: Get data collection rules by subscription ID</span></span>
```
PS C:\>Get-AzDataCollectionRule

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="0161d-115">Mit diesem Befehl werden alle Datensammlungsregeln für das aktuelle Abonnement aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="0161d-115">This command lists all the data collection rules for the current subscription.</span></span>

### <span data-ttu-id="0161d-116">Beispiel 2: Datensammlungsregeln für die angegebene Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="0161d-116">Example 2: Get data collection rules for the given resource group</span></span>
```
PS C:\>Get-AzDataCollectionRule -ResourceGroup "testgroup"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="0161d-117">Mit diesem Befehl werden Datensammlungsregeln für die angegebene Ressourcengruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="0161d-117">This command lists data collection rules for the given resource group.</span></span>

### <span data-ttu-id="0161d-118">Beispiel 3: Erhalten einer Datensammlungsregel</span><span class="sxs-lookup"><span data-stu-id="0161d-118">Example 3: Get a data collection rule</span></span>
```
PS C:\>Get-AzDataCollectionRule -ResourceGroup "testgroup" -RuleName "testDcr"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="0161d-119">Mit diesem Befehl wird eine Datensammlungsregel (eine Liste mit einem einzelnen Element) aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="0161d-119">This command lists one (a list with a single element) data collection rule.</span></span>

### <span data-ttu-id="0161d-120">Beispiel 4: Erhalten einer Datensammlungsregel nach Regel-ID</span><span class="sxs-lookup"><span data-stu-id="0161d-120">Example 4: Get a data collection rule by Rule ID</span></span>
```
PS C:\>Get-AzDataCollectionRule -RuleId "/subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="0161d-121">Mit diesem Befehl wird eine Datensammlungsregel (eine Liste mit einem einzelnen Element) aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="0161d-121">This command lists one (a list with a single element) data collection rule.</span></span>

## <span data-ttu-id="0161d-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0161d-122">PARAMETERS</span></span>

### <span data-ttu-id="0161d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0161d-123">-DefaultProfile</span></span>
<span data-ttu-id="0161d-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0161d-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0161d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0161d-125">-ResourceGroupName</span></span>
<span data-ttu-id="0161d-126">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="0161d-126">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0161d-127">-RuleName</span><span class="sxs-lookup"><span data-stu-id="0161d-127">-RuleName</span></span>
<span data-ttu-id="0161d-128">Der Name der Ressource.</span><span class="sxs-lookup"><span data-stu-id="0161d-128">The name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0161d-129">-RuleId</span><span class="sxs-lookup"><span data-stu-id="0161d-129">-RuleId</span></span>
<span data-ttu-id="0161d-130">Die ID der Ressource.</span><span class="sxs-lookup"><span data-stu-id="0161d-130">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0161d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0161d-131">CommonParameters</span></span>
<span data-ttu-id="0161d-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0161d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0161d-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0161d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0161d-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0161d-134">INPUTS</span></span>

### <span data-ttu-id="0161d-135">System.String</span><span class="sxs-lookup"><span data-stu-id="0161d-135">System.String</span></span>

## <span data-ttu-id="0161d-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0161d-136">OUTPUTS</span></span>

### <span data-ttu-id="0161d-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="0161d-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="0161d-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0161d-138">NOTES</span></span>

## <span data-ttu-id="0161d-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0161d-139">RELATED LINKS</span></span>

<span data-ttu-id="0161d-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="0161d-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>
