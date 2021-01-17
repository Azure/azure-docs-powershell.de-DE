---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 1c5e14fa71ded51d91792f462d01cb463ff36c61
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460531"
---
# <span data-ttu-id="fc397-101">New-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="fc397-101">New-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="fc397-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc397-102">SYNOPSIS</span></span>
<span data-ttu-id="fc397-103">Erstellen Sie eine Ereignisquelle unter der angegebenen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="fc397-103">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="fc397-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc397-104">SYNTAX</span></span>

### <span data-ttu-id="fc397-105">eventhub (Standard)</span><span class="sxs-lookup"><span data-stu-id="fc397-105">eventhub (Default)</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventHubName <String> -EventSourceResourceId <String> -KeyName <String>
 -Kind <Kind> -Location <String> -ServiceBusNameSpace <String> -SharedAccessKey <SecureString>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fc397-106">Othub</span><span class="sxs-lookup"><span data-stu-id="fc397-106">iothub</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventSourceResourceId <String> -IoTHubName <String> -KeyName <String>
 -Kind <Kind> -Location <String> -SharedAccessKey <SecureString> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fc397-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fc397-107">DESCRIPTION</span></span>
<span data-ttu-id="fc397-108">Erstellen Sie eine Ereignisquelle unter der angegebenen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="fc397-108">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="fc397-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fc397-109">EXAMPLES</span></span>

### <span data-ttu-id="fc397-110">Beispiel 1: Erstellen einer Ereignishubereignisquelle in der angegebenen Umgebung</span><span class="sxs-lookup"><span data-stu-id="fc397-110">Example 1: Create an eventhub event source under the specified environment</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -Name spacename002 -ResourceGroupName testgroup -Location eastus
PS C:\> $ev = New-AzEventHub -ResourceGroupName testgroup -NamespaceName spacename002 -Name hubname001 -MessageRetentionInDays 3 -PartitionCount 2
PS C:\> $ks = Get-AzEventHubKey -ResourceGroupName testgroup -NamespaceName spacename002 -AuthorizationRuleName RootManageSharedAccessKey
PS C:\> $k  = $ks.PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name estest001 -EnvironmentName tsitest001 -Kind Microsoft.EventHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -ServiceBusNameSpace spacename002 -EventHubName hubname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Kind               Location Name      Type
----               -------- ----      ----
Microsoft.EventHub eastus   estest001 Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="fc397-111">Mit diesem Befehl wird eine Ereignishubereignisquelle unter der angegebenen Umgebung erstellt.</span><span class="sxs-lookup"><span data-stu-id="fc397-111">This command creates an eventhub event source under the specified environment.</span></span>

### <span data-ttu-id="fc397-112">Beispiel 2: Erstellen einerOthub-Ereignisquelle in der angegebenen Umgebung</span><span class="sxs-lookup"><span data-stu-id="fc397-112">Example 2: Create an iothub event source under the specified environment</span></span>
```powershell
PS C:\> $ev = New-AzIotHub -ResourceGroupName testgroup -Location eastus -Name iotname001 -SkuName S1 -Units 100
PS C:\> $ks = Get-AzIotHubKey -ResourceGroupName testgroup -Name iotname001
PS C:\> $k  = $ks[0].PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name iots001 -EnvironmentName tsitest001 -Kind Microsoft.IoTHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -IoTHubName iotname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Location Name    Type                                                   Kind
-------- ----    ----                                                   ----
eastus   iots001 Microsoft.TimeSeriesInsights/Environments/EventSources Microsoft.IoTHub
```

<span data-ttu-id="fc397-113">Mit diesem Befehl wird eineOthubereignisquelle in der angegebenen Umgebung erstellt.</span><span class="sxs-lookup"><span data-stu-id="fc397-113">This command creates an iothub event source under the specified environment.</span></span>

## <span data-ttu-id="fc397-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc397-114">PARAMETERS</span></span>

### <span data-ttu-id="fc397-115">-ConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="fc397-115">-ConsumerGroupName</span></span>
<span data-ttu-id="fc397-116">Der Name der Consumergruppe des Ereignis-/iot-Hubs, die die Partitionen enthält, aus denen Ereignisse gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="fc397-116">The name of the event/iot hub's consumer group that holds the partitions from which events will be read.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc397-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc397-117">-DefaultProfile</span></span>
<span data-ttu-id="fc397-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fc397-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc397-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="fc397-119">-EnvironmentName</span></span>
<span data-ttu-id="fc397-120">Der Name der Zeitreiheneinblicke-Umgebung, die der angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fc397-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc397-121">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="fc397-121">-EventHubName</span></span>
<span data-ttu-id="fc397-122">Der Name des Ereignishubs.</span><span class="sxs-lookup"><span data-stu-id="fc397-122">The name of the event hub.</span></span>

```yaml
Type: System.String
Parameter Sets: eventhub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc397-123">-EventSourceResourceId</span><span class="sxs-lookup"><span data-stu-id="fc397-123">-EventSourceResourceId</span></span>
<span data-ttu-id="fc397-124">Die Ressourcen-ID der Ereignisquelle im Azure-Ressourcen-Manager.</span><span class="sxs-lookup"><span data-stu-id="fc397-124">The resource id of the event source in Azure Resource Manager.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc397-125">-IoTHubName</span><span class="sxs-lookup"><span data-stu-id="fc397-125">-IoTHubName</span></span>
<span data-ttu-id="fc397-126">Der Name des iot-Hubs.</span><span class="sxs-lookup"><span data-stu-id="fc397-126">The name of the iot hub.</span></span>

```yaml
Type: System.String
Parameter Sets: iothub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc397-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="fc397-127">-KeyName</span></span>
<span data-ttu-id="fc397-128">Der Name des SAS-Schlüssels, der dem Time Series Insights-Dienst Zugriff auf das Ereignis bzw. den iot-Hub gewährt.</span><span class="sxs-lookup"><span data-stu-id="fc397-128">The name of the SAS key that grants the Time Series Insights service access to the event/iot hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc397-129">-Kind</span><span class="sxs-lookup"><span data-stu-id="fc397-129">-Kind</span></span>
<span data-ttu-id="fc397-130">Die Art der Ereignisquelle.</span><span class="sxs-lookup"><span data-stu-id="fc397-130">The kind of the event source.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc397-131">-Location</span><span class="sxs-lookup"><span data-stu-id="fc397-131">-Location</span></span>
<span data-ttu-id="fc397-132">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="fc397-132">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc397-133">-Name</span><span class="sxs-lookup"><span data-stu-id="fc397-133">-Name</span></span>
<span data-ttu-id="fc397-134">Der Name der Ereignisquelle.</span><span class="sxs-lookup"><span data-stu-id="fc397-134">Name of the event source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc397-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc397-135">-ResourceGroupName</span></span>
<span data-ttu-id="fc397-136">Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fc397-136">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc397-137">-ServiceBusNameSpace</span><span class="sxs-lookup"><span data-stu-id="fc397-137">-ServiceBusNameSpace</span></span>
<span data-ttu-id="fc397-138">Der Name des Dienstbus, der den Ereignishub enthält.</span><span class="sxs-lookup"><span data-stu-id="fc397-138">The name of the service bus that contains the event hub.</span></span>

```yaml
Type: System.String
Parameter Sets: eventhub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc397-139">-SharedAccessKey</span><span class="sxs-lookup"><span data-stu-id="fc397-139">-SharedAccessKey</span></span>
<span data-ttu-id="fc397-140">Der Wert des freigegebenen Zugriffsschlüssels, der dem Time Series Insights-Dienst Lesezugriff auf das Ereignis bzw. den iot-Hub gewährt.</span><span class="sxs-lookup"><span data-stu-id="fc397-140">The value of the shared access key that grants the Time Series Insights service read access to the event/iot hub.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc397-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fc397-141">-SubscriptionId</span></span>
<span data-ttu-id="fc397-142">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="fc397-142">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc397-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="fc397-143">-Tag</span></span>
<span data-ttu-id="fc397-144">Schlüssel-Wert-Paare zusätzlicher Eigenschaften für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="fc397-144">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="fc397-145">-TimeStampPropertyName</span><span class="sxs-lookup"><span data-stu-id="fc397-145">-TimeStampPropertyName</span></span>
<span data-ttu-id="fc397-146">Die Ereigniseigenschaft, die als Zeitstempel der Ereignisquelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fc397-146">The event property that will be used as the event source's timestamp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc397-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc397-147">-Confirm</span></span>
<span data-ttu-id="fc397-148">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fc397-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc397-149">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fc397-149">-WhatIf</span></span>
<span data-ttu-id="fc397-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fc397-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc397-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fc397-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc397-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc397-152">CommonParameters</span></span>
<span data-ttu-id="fc397-153">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc397-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc397-154">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc397-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc397-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fc397-155">INPUTS</span></span>

## <span data-ttu-id="fc397-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fc397-156">OUTPUTS</span></span>

### <span data-ttu-id="fc397-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="fc397-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="fc397-158">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fc397-158">NOTES</span></span>

<span data-ttu-id="fc397-159">ALIASE</span><span class="sxs-lookup"><span data-stu-id="fc397-159">ALIASES</span></span>

## <span data-ttu-id="fc397-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fc397-160">RELATED LINKS</span></span>

