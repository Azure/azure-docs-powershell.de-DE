---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 5590a89b22c0adc3dfb2df88e6b977dec268a822
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178112"
---
# <span data-ttu-id="3d76c-101">Get-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="3d76c-101">Get-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="3d76c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3d76c-102">SYNOPSIS</span></span>
<span data-ttu-id="3d76c-103">Ruft die Ereignisquelle mit dem angegebenen Namen in der angegebenen Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="3d76c-103">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="3d76c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d76c-104">SYNTAX</span></span>

### <span data-ttu-id="3d76c-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="3d76c-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3d76c-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="3d76c-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3d76c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3d76c-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d76c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d76c-108">DESCRIPTION</span></span>
<span data-ttu-id="3d76c-109">Ruft die Ereignisquelle mit dem angegebenen Namen in der angegebenen Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="3d76c-109">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="3d76c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d76c-110">EXAMPLES</span></span>

### <span data-ttu-id="3d76c-111">Beispiel 1: Auflisten aller Ereignisquellen unter der angegebenen Umgebung</span><span class="sxs-lookup"><span data-stu-id="3d76c-111">Example 1: List all event sources under the specified environment</span></span>
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

<span data-ttu-id="3d76c-112">Dieser Befehl listet alle Ereignisquellen in den angegebenen Umgebungen auf.</span><span class="sxs-lookup"><span data-stu-id="3d76c-112">This command lists all event sources under the specified environments.</span></span>

### <span data-ttu-id="3d76c-113">Beispiel 2: Abrufen einer angegebenen Ereignisquelle anhand des Namens</span><span class="sxs-lookup"><span data-stu-id="3d76c-113">Example 2: Get a specified event source by name</span></span>
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

<span data-ttu-id="3d76c-114">Mit diesem Befehl wird eine bestimmte Ereignisquelle abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3d76c-114">This command gets a specific event source.</span></span>

### <span data-ttu-id="3d76c-115">Beispiel 3: Abrufen einer angegebenen Ereignisquelle nach Objekt</span><span class="sxs-lookup"><span data-stu-id="3d76c-115">Example 3: Get a specified event source by object</span></span>
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

<span data-ttu-id="3d76c-116">Mit diesem Befehl wird eine bestimmte Ereignisquelle abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3d76c-116">This command gets a specific event source.</span></span>

## <span data-ttu-id="3d76c-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d76c-117">PARAMETERS</span></span>

### <span data-ttu-id="3d76c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d76c-118">-DefaultProfile</span></span>
<span data-ttu-id="3d76c-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3d76c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d76c-120">-Umgebungsname</span><span class="sxs-lookup"><span data-stu-id="3d76c-120">-EnvironmentName</span></span>
<span data-ttu-id="3d76c-121">Der Name der Zeitreihen Einblicke-Umgebung, die der angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3d76c-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="3d76c-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3d76c-122">-InputObject</span></span>
<span data-ttu-id="3d76c-123">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="3d76c-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3d76c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3d76c-124">-Name</span></span>
<span data-ttu-id="3d76c-125">Der Name der Ereignisquelle für Zeitreihen Einblicke, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3d76c-125">The name of the Time Series Insights event source associated with the specified environment.</span></span>

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

### <span data-ttu-id="3d76c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d76c-126">-ResourceGroupName</span></span>
<span data-ttu-id="3d76c-127">Der Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3d76c-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="3d76c-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="3d76c-128">-SubscriptionId</span></span>
<span data-ttu-id="3d76c-129">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="3d76c-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="3d76c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d76c-130">CommonParameters</span></span>
<span data-ttu-id="3d76c-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d76c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d76c-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d76c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d76c-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3d76c-133">INPUTS</span></span>

### <span data-ttu-id="3d76c-134">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="3d76c-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="3d76c-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3d76c-135">OUTPUTS</span></span>

### <span data-ttu-id="3d76c-136">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. Api20200515. IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="3d76c-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="3d76c-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="3d76c-137">NOTES</span></span>

<span data-ttu-id="3d76c-138">Aliase</span><span class="sxs-lookup"><span data-stu-id="3d76c-138">ALIASES</span></span>

<span data-ttu-id="3d76c-139">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3d76c-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3d76c-140">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3d76c-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3d76c-141">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="3d76c-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3d76c-142">Inputobject <ITimeSeriesInsightsIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="3d76c-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3d76c-143">`[AccessPolicyName <String>]`: Name der Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="3d76c-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="3d76c-144">`[EnvironmentName <String>]`: Name der Umgebung</span><span class="sxs-lookup"><span data-stu-id="3d76c-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="3d76c-145">`[EventSourceName <String>]`: Der Name der Ereignisquelle für Zeitreihen Einblicke, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3d76c-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="3d76c-146">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="3d76c-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3d76c-147">`[ReferenceDataSetName <String>]`: Name des referenzdatensatzes.</span><span class="sxs-lookup"><span data-stu-id="3d76c-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="3d76c-148">`[ResourceGroupName <String>]`: Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3d76c-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="3d76c-149">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="3d76c-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="3d76c-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3d76c-150">RELATED LINKS</span></span>

