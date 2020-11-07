---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 989CE245-FD1D-4E1D-90A2-2D7DA3975D0B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermautoscalesetting
schema: 2.0.0
ms.openlocfilehash: f11a1198485f7c138ba59f740b0e2144f70ba3a5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850012"
---
# <span data-ttu-id="75214-101">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="75214-101">Get-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="75214-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75214-102">SYNOPSIS</span></span>
<span data-ttu-id="75214-103">Ruft AutoScale-Einstellungen ab.</span><span class="sxs-lookup"><span data-stu-id="75214-103">Gets Autoscale settings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75214-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75214-104">SYNTAX</span></span>

```
Get-AzureRmAutoscaleSetting -ResourceGroupName <String> [-Name <String>] [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75214-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75214-105">DESCRIPTION</span></span>
<span data-ttu-id="75214-106">Das Cmdlet " **Get-AzureRmAutoscaleSetting** " ruft alle AutoScale-Einstellungen ab, die einer Ressourcengruppe oder einer angegebenen AutoScale-Einstellung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="75214-106">The **Get-AzureRmAutoscaleSetting** cmdlet gets all Autoscale settings associated with a resource group or a specified Autoscale setting.</span></span>

## <span data-ttu-id="75214-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75214-107">EXAMPLES</span></span>

### <span data-ttu-id="75214-108">Beispiel 1: Abrufen von Einstellungen für das AutoSkalieren</span><span class="sxs-lookup"><span data-stu-id="75214-108">Example 1: Get Autoscale settings</span></span>
```
PS C:\>Get-AzureRmAutoscaleSetting -ResourceGroup "Default-Web-EastUS" -DetailedOutput
resourceId : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft. 
             insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS
Location   : East US
Name       : DefaultServerFarm-Default-Web-EastUS
Properties : 
Enabled    : True
Profiles   : 
Capacity   : 
Default    : 1
Minimum    : 3
Maximum    : 1
FixedDate     : 
Name          : No scheduled times
Recurrence    : 
Rules         : 
MetricTrigger : 
MetricName         : CpuPercentage
MetricResourceId   : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : GreaterThanOrEqual
Statistic          : Average
Threshold          : 14
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:45:00
ScaleAction        : 
Cooldown   : 00:05:00
Direction  : Increase
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : CpuPercentage
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : LessThanOrEqual
Statistic          : Average
Threshold          : 4
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:45:00
ScaleAction  : 
Cooldown   : 02:00:00
Direction  : Decrease
Type       : ChangeCount
Value      : 1

MetricTrigger  : 
MetricName         : BytesReceived
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : LessThanOrEqual
Statistic          : Average
Threshold          : 50
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:10:00
ScaleAction    : 
Cooldown   : 00:10:00
Direction  : Decrease
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : BytesReceived
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : GreaterThanOrEqual
Statistic          : Average
Threshold          : 100
                                                TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:05:00
ScaleAction    : 
Cooldown   : 00:10:00
                                                Direction  : Increase
Type       : ChangeCount
Value      : 1
             TargetResourceId : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/
             providers/microsoft.web/serverFarms/DefaultServerFarm
Tags       : {[$type, Microsoft.WindowsAzure.Management.Common.Storage.CasePreservedDictionary, 
             Microsoft.WindowsAzure.Management.Common.Storage], [hidden-link:/subscriptions/a93fb07c-6c93-40be-bf3b-4f0
             deba10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm, 
             Resource]}
```

<span data-ttu-id="75214-109">Dieser Befehl ruft die Einstellungen für die autoskala ab, die der Ressourcengruppe Default-Web-eastus zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="75214-109">This command gets the Autoscale settings assigned to the resource group Default-Web-EastUS.</span></span>

### <span data-ttu-id="75214-110">Beispiel 2: Abrufen einer AutoScale-Einstellung nach Name</span><span class="sxs-lookup"><span data-stu-id="75214-110">Example 2: Get an Autoscale setting by name</span></span>
```
PS C:\>Get-AzureRmAutoscaleSetting -ResourceGroupName "Default-Web-EastUS" -Name "DefaultServerFarm-Default-Web-EastUS" -DetailedOutput
resourceId : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft. 
             insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS
Location   : East US
Name       : DefaultServerFarm-Default-Web-EastUS
Properties : 
Enabled    : True
Profiles   : 
Capacity   : 
Default    : 1
Minimum    : 3
Maximum    : 1
FixedDate     : 
Name          : No scheduled times
Recurrence    : 
Rules         : 
MetricTrigger : 
MetricName         : CpuPercentage
MetricResourceId   : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : GreaterThanOrEqual
Statistic          : Average
Threshold          : 14
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:45:00
ScaleAction    : 
Cooldown   : 00:05:00
Direction  : Increase
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : CpuPercentage
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : LessThanOrEqual
Statistic          : Average
Threshold          : 4
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:45:00
ScaleAction    : 
Cooldown   : 02:00:00
Direction  : Decrease
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : BytesReceived
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : LessThanOrEqual
Statistic          : Average
Threshold          : 50
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:10:00
ScaleAction    : 
Cooldown   : 00:10:00
Direction  : Decrease
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : BytesReceived
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : GreaterThanOrEqual
Statistic          : Average
Threshold          : 100
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:05:00
ScaleAction    : 
Cooldown   : 00:10:00
Direction  : Increase
Type       : ChangeCount
Value      : 1
TargetResourceId : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/
             providers/microsoft.web/serverFarms/DefaultServerFarm
Tags       : {[$type, Microsoft.WindowsAzure.Management.Common.Storage.CasePreservedDictionary, 
             Microsoft.WindowsAzure.Management.Common.Storage], [hidden-link:/subscriptions/a93fb07c-6c93-40be-bf3b-4f0
             deba10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm, 
             Resource]}
```

<span data-ttu-id="75214-111">Dieser Befehl ruft die Einstellung AutoScale mit dem Namen DefaultServerFarm-Default-Web-eastus ab.</span><span class="sxs-lookup"><span data-stu-id="75214-111">This command gets the Autoscale setting named DefaultServerFarm-Default-Web-EastUS.</span></span>

## <span data-ttu-id="75214-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="75214-112">PARAMETERS</span></span>

### <span data-ttu-id="75214-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75214-113">-DefaultProfile</span></span>
<span data-ttu-id="75214-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="75214-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75214-115">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="75214-115">-DetailedOutput</span></span>
<span data-ttu-id="75214-116">Gibt an, dass dieser Vorgang alle Details in der Ausgabe anzeigt.</span><span class="sxs-lookup"><span data-stu-id="75214-116">Indicates that this operation displays full details in the output.</span></span>

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

### <span data-ttu-id="75214-117">-Name</span><span class="sxs-lookup"><span data-stu-id="75214-117">-Name</span></span>
<span data-ttu-id="75214-118">Gibt den Namen der abzurufenden Einstellung an.</span><span class="sxs-lookup"><span data-stu-id="75214-118">Specifies the name of the setting to get.</span></span>

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

### <span data-ttu-id="75214-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75214-119">-ResourceGroupName</span></span>
<span data-ttu-id="75214-120">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="75214-120">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75214-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75214-121">CommonParameters</span></span>
<span data-ttu-id="75214-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75214-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75214-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75214-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75214-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75214-124">INPUTS</span></span>

### <span data-ttu-id="75214-125">System. String</span><span class="sxs-lookup"><span data-stu-id="75214-125">System.String</span></span>

### <span data-ttu-id="75214-126">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="75214-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="75214-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75214-127">OUTPUTS</span></span>

### <span data-ttu-id="75214-128">Microsoft. Azure. Commands. Insights. OutputClasses. PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="75214-128">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

## <span data-ttu-id="75214-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="75214-129">NOTES</span></span>

## <span data-ttu-id="75214-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75214-130">RELATED LINKS</span></span>

[<span data-ttu-id="75214-131">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="75214-131">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="75214-132">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="75214-132">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


