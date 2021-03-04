---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: c28d33e4da860a68227228564c55a151a3068329
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931424"
---
# <span data-ttu-id="b537c-101">Get-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="b537c-101">Get-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="b537c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b537c-102">SYNOPSIS</span></span>
<span data-ttu-id="b537c-103">Ruft die Ereignisquelle mit dem angegebenen Namen in der angegebenen Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="b537c-103">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="b537c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b537c-104">SYNTAX</span></span>

### <span data-ttu-id="b537c-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="b537c-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b537c-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="b537c-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b537c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b537c-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b537c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b537c-108">DESCRIPTION</span></span>
<span data-ttu-id="b537c-109">Ruft die Ereignisquelle mit dem angegebenen Namen in der angegebenen Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="b537c-109">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="b537c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b537c-110">EXAMPLES</span></span>

### <span data-ttu-id="b537c-111">Beispiel 1: Auflisten aller Ereignisquellen unter der angegebenen Umgebung</span><span class="sxs-lookup"><span data-stu-id="b537c-111">Example 1: List all event sources under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -EnvironmentName tsitest001

ConsumerGroupName     : testgroup2
EventHubName          : hubname001
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.EventHub/namespaces/spacename001/eventhubs/hu 
                        bname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve 
                        ntsources/estest001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.EventHub
Location              : eastus
Name                  : estest001
ServiceBusNamespace   : spacename001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve 
                        ntsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="b537c-112">Mit diesem Befehl werden alle Ereignisquellen unter den angegebenen Umgebungen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b537c-112">This command lists all event sources under the specified environments.</span></span>

### <span data-ttu-id="b537c-113">Beispiel 2: Erhalten einer angegebenen Ereignisquelle nach Name</span><span class="sxs-lookup"><span data-stu-id="b537c-113">Example 2: Get a specified event source by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -EnvironmentName tsitest001 -Name iots001

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve
                        ntsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="b537c-114">Dieser Befehl ruft eine bestimmte Ereignisquelle ab.</span><span class="sxs-lookup"><span data-stu-id="b537c-114">This command gets a specific event source.</span></span>

### <span data-ttu-id="b537c-115">Beispiel 3: Erhalten einer angegebenen Ereignisquelle nach Objekt</span><span class="sxs-lookup"><span data-stu-id="b537c-115">Example 3: Get a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsi-esrfyi9h
PS C:\> Get-AzTimeSeriesInsightsEventSource -InputObject $es

ConsumerGroupName     : tsi-test-i01k5l
EventHubName          : eventhubname-d2rvmp
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.EventHub/namespaces/eventhubspace-0t3khp/eventhubs/eventhubname-d2rvmp
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.TimeSeriesInsights/environments/tsi-envv8u56x/eventsources/tsi-esrfyi9h
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.EventHub
Location              : eastus2
Name                  : tsi-esrfyi9h
ServiceBusNamespace   : eventhubspace-0t3khp
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="b537c-116">Dieser Befehl ruft eine bestimmte Ereignisquelle ab.</span><span class="sxs-lookup"><span data-stu-id="b537c-116">This command gets a specific event source.</span></span>

## <span data-ttu-id="b537c-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b537c-117">PARAMETERS</span></span>

### <span data-ttu-id="b537c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b537c-118">-DefaultProfile</span></span>
<span data-ttu-id="b537c-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b537c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b537c-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="b537c-120">-EnvironmentName</span></span>
<span data-ttu-id="b537c-121">Der Name der Zeitreiheneinblickumgebung, die der angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b537c-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b537c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b537c-122">-InputObject</span></span>
<span data-ttu-id="b537c-123">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="b537c-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b537c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b537c-124">-Name</span></span>
<span data-ttu-id="b537c-125">Der Name der Time Series Insights-Ereignisquelle, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b537c-125">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b537c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b537c-126">-ResourceGroupName</span></span>
<span data-ttu-id="b537c-127">Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b537c-127">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b537c-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b537c-128">-SubscriptionId</span></span>
<span data-ttu-id="b537c-129">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="b537c-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b537c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b537c-130">CommonParameters</span></span>
<span data-ttu-id="b537c-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b537c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b537c-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b537c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b537c-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b537c-133">INPUTS</span></span>

### <span data-ttu-id="b537c-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="b537c-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="b537c-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b537c-135">OUTPUTS</span></span>

### <span data-ttu-id="b537c-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="b537c-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="b537c-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b537c-137">NOTES</span></span>

<span data-ttu-id="b537c-138">ALIASE</span><span class="sxs-lookup"><span data-stu-id="b537c-138">ALIASES</span></span>

<span data-ttu-id="b537c-139">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="b537c-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b537c-140">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="b537c-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b537c-141">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b537c-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b537c-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="b537c-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b537c-143">`[AccessPolicyName <String>]`: Name der Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="b537c-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="b537c-144">`[EnvironmentName <String>]`: Name der Umgebung</span><span class="sxs-lookup"><span data-stu-id="b537c-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="b537c-145">`[EventSourceName <String>]`: Der Name der Time Series Insights-Ereignisquelle, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b537c-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="b537c-146">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="b537c-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b537c-147">`[ReferenceDataSetName <String>]`: Name des Bezugsdatensets.</span><span class="sxs-lookup"><span data-stu-id="b537c-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="b537c-148">`[ResourceGroupName <String>]`: Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b537c-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="b537c-149">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="b537c-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="b537c-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b537c-150">RELATED LINKS</span></span>

