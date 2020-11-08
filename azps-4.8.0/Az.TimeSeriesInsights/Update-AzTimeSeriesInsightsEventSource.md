---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: e87487e55ce285aa5c430dabaa274ee70c34ba00
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165419"
---
# <span data-ttu-id="a0e7a-101">Update-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="a0e7a-101">Update-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="a0e7a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a0e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="a0e7a-103">Aktualisiert die Ereignisquelle mit dem angegebenen Namen im angegebenen Abonnement, in der Ressourcengruppe und in der Umgebung.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-103">Updates the event source with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="a0e7a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0e7a-104">SYNTAX</span></span>

### <span data-ttu-id="a0e7a-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0e7a-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="a0e7a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a0e7a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a0e7a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0e7a-107">DESCRIPTION</span></span>
<span data-ttu-id="a0e7a-108">Aktualisiert die Ereignisquelle mit dem angegebenen Namen im angegebenen Abonnement, in der Ressourcengruppe und in der Umgebung.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-108">Updates the event source with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="a0e7a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a0e7a-109">EXAMPLES</span></span>

### <span data-ttu-id="a0e7a-110">Beispiel 1: Aktualisieren einer angegebenen Ereignisquelle anhand des Namens</span><span class="sxs-lookup"><span data-stu-id="a0e7a-110">Example 1: Update a specified event source by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup -Tag @{"tgk"="001"}

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eventsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="a0e7a-111">Mit diesem Befehl wird eine bestimmte Ereignisquelle aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-111">This command updates a specific event source.</span></span>

### <span data-ttu-id="a0e7a-112">Beispiel 3: Aktualisieren einer angegebenen Ereignisquelle nach Objekt</span><span class="sxs-lookup"><span data-stu-id="a0e7a-112">Example 3: Update a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Update-AzTimeSeriesInsightsEventSource -InputObject $es -Tag @{"tgb"="002"}

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eventsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="a0e7a-113">Mit diesem Befehl wird eine bestimmte Ereignisquelle aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-113">This command updates a specific event source.</span></span>

## <span data-ttu-id="a0e7a-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0e7a-114">PARAMETERS</span></span>

### <span data-ttu-id="a0e7a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0e7a-115">-DefaultProfile</span></span>
<span data-ttu-id="a0e7a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0e7a-117">-Umgebungsname</span><span class="sxs-lookup"><span data-stu-id="a0e7a-117">-EnvironmentName</span></span>
<span data-ttu-id="a0e7a-118">Der Name der Zeitreihen Einblicke-Umgebung, die der angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0e7a-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a0e7a-119">-InputObject</span></span>
<span data-ttu-id="a0e7a-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0e7a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a0e7a-121">-Name</span></span>
<span data-ttu-id="a0e7a-122">Der Name der Ereignisquelle für Zeitreihen Einblicke, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0e7a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0e7a-123">-ResourceGroupName</span></span>
<span data-ttu-id="a0e7a-124">Der Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-124">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0e7a-125">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="a0e7a-125">-SubscriptionId</span></span>
<span data-ttu-id="a0e7a-126">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0e7a-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="a0e7a-127">-Tag</span></span>
<span data-ttu-id="a0e7a-128">Schlüssel-Wert-Paare zusätzlicher Eigenschaften für die Ereignisquelle.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-128">Key-value pairs of additional properties for the event source.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0e7a-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a0e7a-129">-Confirm</span></span>
<span data-ttu-id="a0e7a-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0e7a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0e7a-131">-WhatIf</span></span>
<span data-ttu-id="a0e7a-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0e7a-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0e7a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0e7a-134">CommonParameters</span></span>
<span data-ttu-id="a0e7a-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0e7a-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0e7a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0e7a-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a0e7a-137">INPUTS</span></span>

### <span data-ttu-id="a0e7a-138">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="a0e7a-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="a0e7a-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a0e7a-139">OUTPUTS</span></span>

### <span data-ttu-id="a0e7a-140">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. Api20200515. IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="a0e7a-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="a0e7a-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="a0e7a-141">NOTES</span></span>

<span data-ttu-id="a0e7a-142">Aliase</span><span class="sxs-lookup"><span data-stu-id="a0e7a-142">ALIASES</span></span>

<span data-ttu-id="a0e7a-143">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a0e7a-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a0e7a-144">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a0e7a-145">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a0e7a-146">Inputobject <ITimeSeriesInsightsIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="a0e7a-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a0e7a-147">`[AccessPolicyName <String>]`: Name der Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="a0e7a-148">`[EnvironmentName <String>]`: Name der Umgebung</span><span class="sxs-lookup"><span data-stu-id="a0e7a-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="a0e7a-149">`[EventSourceName <String>]`: Der Name der Ereignisquelle für Zeitreihen Einblicke, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="a0e7a-150">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="a0e7a-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a0e7a-151">`[ReferenceDataSetName <String>]`: Name des referenzdatensatzes.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="a0e7a-152">`[ResourceGroupName <String>]`: Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="a0e7a-153">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="a0e7a-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a0e7a-154">RELATED LINKS</span></span>

