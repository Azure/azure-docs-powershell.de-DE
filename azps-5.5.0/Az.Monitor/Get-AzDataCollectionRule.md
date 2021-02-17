---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRule.md
ms.openlocfilehash: 8826dfdf8fe0152035319c576210088bcd5521e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147425"
---
# <span data-ttu-id="fe3f6-101">Get-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="fe3f6-101">Get-AzDataCollectionRule</span></span>

## <span data-ttu-id="fe3f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe3f6-102">SYNOPSIS</span></span>
<span data-ttu-id="fe3f6-103">Ruft Datensammlungsregel(en) ab.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-103">Gets data collection rule(s).</span></span>

## <span data-ttu-id="fe3f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe3f6-104">SYNTAX</span></span>

### <span data-ttu-id="fe3f6-105">BySubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="fe3f6-105">BySubscription (Default)</span></span>
```
Get-AzDataCollectionRule
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="fe3f6-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fe3f6-106">ByResourceGroup</span></span>
```
Get-AzDataCollectionRule
   -ResourceGroupName <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="fe3f6-107">ByName</span><span class="sxs-lookup"><span data-stu-id="fe3f6-107">ByName</span></span>
```
Get-AzDataCollectionRule
   -ResourceGroupName <string>
   -RuleName <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="fe3f6-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fe3f6-108">ByResourceId</span></span>
```
Get-AzDataCollectionRule
   -RuleId <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

## <span data-ttu-id="fe3f6-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fe3f6-109">DESCRIPTION</span></span>
<span data-ttu-id="fe3f6-110">Das **Cmdlet "Get-AzDataCollectionRule"** ruft mindestens eine Datensammlungsregeln ab.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-110">The **Get-AzDataCollectionRule** cmdlet gets one or more data collection rules.</span></span>

<span data-ttu-id="fe3f6-111">Datensammlungsregeln (Data Collection Rules, DCR) definieren Daten, die in Azure Monitor übermittelt werden, und geben an, wohin diese Daten gesendet oder gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-111">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="fe3f6-112">Hier finden Sie den vollständigen [DcR-Übersichtsartikel.](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="fe3f6-112">Here is the complete [DCR overview article](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="fe3f6-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fe3f6-113">EXAMPLES</span></span>

### <span data-ttu-id="fe3f6-114">Beispiel 1: Datensammlungsregeln nach Abonnement-ID erhalten</span><span class="sxs-lookup"><span data-stu-id="fe3f6-114">Example 1: Get data collection rules by subscription ID</span></span>
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

<span data-ttu-id="fe3f6-115">Dieser Befehl listet alle Datensammlungsregeln für das aktuelle Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-115">This command lists all the data collection rules for the current subscription.</span></span>

### <span data-ttu-id="fe3f6-116">Beispiel 2: Datensammlungsregeln für die angegebene Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="fe3f6-116">Example 2: Get data collection rules for the given resource group</span></span>
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

<span data-ttu-id="fe3f6-117">Dieser Befehl listet Datensammlungsregeln für die angegebene Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-117">This command lists data collection rules for the given resource group.</span></span>

### <span data-ttu-id="fe3f6-118">Beispiel 3: Erhalten einer Datensammlungsregel</span><span class="sxs-lookup"><span data-stu-id="fe3f6-118">Example 3: Get a data collection rule</span></span>
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

<span data-ttu-id="fe3f6-119">Dieser Befehl listet eine Datensammlungsregel (eine Liste mit einem einzelnen Element) auf.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-119">This command lists one (a list with a single element) data collection rule.</span></span>

### <span data-ttu-id="fe3f6-120">Beispiel 4: Erhalten einer Datensammlungsregel nach Regel-ID</span><span class="sxs-lookup"><span data-stu-id="fe3f6-120">Example 4: Get a data collection rule by Rule ID</span></span>
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

<span data-ttu-id="fe3f6-121">Dieser Befehl listet eine Datensammlungsregel (eine Liste mit einem einzelnen Element) auf.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-121">This command lists one (a list with a single element) data collection rule.</span></span>

## <span data-ttu-id="fe3f6-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe3f6-122">PARAMETERS</span></span>

### <span data-ttu-id="fe3f6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe3f6-123">-DefaultProfile</span></span>
<span data-ttu-id="fe3f6-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fe3f6-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe3f6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe3f6-125">-ResourceGroupName</span></span>
<span data-ttu-id="fe3f6-126">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="fe3f6-126">The resource group name</span></span>

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

### <span data-ttu-id="fe3f6-127">-RuleName</span><span class="sxs-lookup"><span data-stu-id="fe3f6-127">-RuleName</span></span>
<span data-ttu-id="fe3f6-128">Der Name der Ressource.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-128">The name of the resource.</span></span>

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

### <span data-ttu-id="fe3f6-129">-RuleId</span><span class="sxs-lookup"><span data-stu-id="fe3f6-129">-RuleId</span></span>
<span data-ttu-id="fe3f6-130">Die ID der Ressource.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-130">The ID of the resource.</span></span>

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

### <span data-ttu-id="fe3f6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe3f6-131">CommonParameters</span></span>
<span data-ttu-id="fe3f6-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe3f6-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe3f6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe3f6-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fe3f6-134">INPUTS</span></span>

### <span data-ttu-id="fe3f6-135">System.String</span><span class="sxs-lookup"><span data-stu-id="fe3f6-135">System.String</span></span>

## <span data-ttu-id="fe3f6-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fe3f6-136">OUTPUTS</span></span>

### <span data-ttu-id="fe3f6-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="fe3f6-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="fe3f6-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fe3f6-138">NOTES</span></span>

## <span data-ttu-id="fe3f6-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fe3f6-139">RELATED LINKS</span></span>

<span data-ttu-id="fe3f6-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="fe3f6-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>
