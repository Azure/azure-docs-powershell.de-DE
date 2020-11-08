---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: f4f42b257c5ce54085214c8cd9d2f79d9e8a6387
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179945"
---
# <span data-ttu-id="4eaeb-101">Get-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="4eaeb-101">Get-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="4eaeb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4eaeb-102">SYNOPSIS</span></span>
<span data-ttu-id="4eaeb-103">Ruft die Umgebung mit dem angegebenen Namen in der angegebenen Abonnement-und Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="4eaeb-103">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="4eaeb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4eaeb-104">SYNTAX</span></span>

### <span data-ttu-id="4eaeb-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="4eaeb-105">List1 (Default)</span></span>
```
Get-AzTimeSeriesInsightsEnvironment [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="4eaeb-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="4eaeb-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4eaeb-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4eaeb-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4eaeb-108">Liste</span><span class="sxs-lookup"><span data-stu-id="4eaeb-108">List</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4eaeb-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4eaeb-109">DESCRIPTION</span></span>
<span data-ttu-id="4eaeb-110">Ruft die Umgebung mit dem angegebenen Namen in der angegebenen Abonnement-und Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="4eaeb-110">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="4eaeb-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4eaeb-111">EXAMPLES</span></span>

### <span data-ttu-id="4eaeb-112">Beispiel 1: Abrufen einer Zeitreihen Einblicke-Umgebung</span><span class="sxs-lookup"><span data-stu-id="4eaeb-112">Example 1: Get a time series insights environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001

DataAccessFqdn               : b6d113a4-0865-405f-b09e-ad4355b5d046.env.timeseries.azure.com
DataAccessId                 : b6d113a4-0865-405f-b09e-ad4355b5d046
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest 
                               001
IngressState                 :
Kind                         : Gen1
Location                     : eastus
Name                         : tsitest001
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 2
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="4eaeb-113">Mit diesem Befehl wird eine Zeitreihen Einblicke-Umgebung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="4eaeb-113">This command gets a time series insights environment.</span></span>

### <span data-ttu-id="4eaeb-114">Beispiel 2: Auflisten aller Zeitreihen Einblicke in Umgebungen</span><span class="sxs-lookup"><span data-stu-id="4eaeb-114">Example 2: List all time series insights environments</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup

DataAccessFqdn                      : 3de1d1e1-4f9b-4bc6-aad3-a835597dcd86.env.timeseries.azure.com
DataAccessId                        : 3de1d1e1-4f9b-4bc6-aad3-a835597dcd86
Id                                  : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/ 
                                      tsill
IngressState                        :
Kind                                : Gen2
Location                            : EastUs
Name                                : tsill
PropertyUsageState                  :
Sku                                 : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                         : 1
SkuName                             : L1
StateDetailCode                     :
StateDetailCurrentCount             :
StateDetailMaxCount                 :
StateDetailMessage                  :
StorageConfigurationAccountName     : cdolauli
Tag                                 : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimeSeriesIdProperty                : {ccc}
Type                                : Microsoft.TimeSeriesInsights/Environments
WarmStoreConfigurationDataRetention : 00:00:00

DataAccessFqdn               : b6d113a4-0865-405f-b09e-ad4355b5d046.env.timeseries.azure.com
DataAccessId                 : b6d113a4-0865-405f-b09e-ad4355b5d046
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest 
                               001
IngressState                 :
Kind                         : Gen1
Location                     : eastus
Name                         : tsitest001
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 2
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="4eaeb-115">Dieser Befehl listet alle Zeitreihen Einblicke-Umgebungen in einer Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="4eaeb-115">This command lists all time series insights environments in a resource group.</span></span>

### <span data-ttu-id="4eaeb-116">Beispiel 3: Abrufen einer Zeitreihen Einblicke-Umgebung nach Objekt</span><span class="sxs-lookup"><span data-stu-id="4eaeb-116">Example 3: Get a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName tsi-test-i01k5l -Name tsi-envv8u56x 
PS C:\> Get-AzTimeSeriesInsightsEnvironment -InputObject $env

DataAccessFqdn               : d76a61f2-8a30-41a5-9587-f241eb9b48d9.env.timeseries.azure.com
DataAccessId                 : d76a61f2-8a30-41a5-9587-f241eb9b48d9
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.TimeSeriesInsights/environments/tsi-envv8u56x
IngressState                 :
Kind                         : Gen1
Location                     : eastus2
Name                         : tsi-envv8u56x
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 1
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="4eaeb-117">Dieser Befehl ruft eine Zeitreihen Einblicke-Umgebungen ab.</span><span class="sxs-lookup"><span data-stu-id="4eaeb-117">This command gets a time series insights environments.</span></span>

## <span data-ttu-id="4eaeb-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="4eaeb-118">PARAMETERS</span></span>

### <span data-ttu-id="4eaeb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eaeb-119">-DefaultProfile</span></span>
<span data-ttu-id="4eaeb-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4eaeb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4eaeb-121">– Erweitern</span><span class="sxs-lookup"><span data-stu-id="4eaeb-121">-Expand</span></span>
<span data-ttu-id="4eaeb-122">Beim Festlegen von $Expand = Status wird der Status der internen Dienste der Umgebung im Time Series Insights-Dienst berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="4eaeb-122">Setting $expand=status will include the status of the internal services of the environment in the Time Series Insights service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eaeb-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4eaeb-123">-InputObject</span></span>
<span data-ttu-id="4eaeb-124">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="4eaeb-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4eaeb-125">-Name</span><span class="sxs-lookup"><span data-stu-id="4eaeb-125">-Name</span></span>
<span data-ttu-id="4eaeb-126">Der Name der Zeitreihen Einblicke-Umgebung, die der angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4eaeb-126">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eaeb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eaeb-127">-ResourceGroupName</span></span>
<span data-ttu-id="4eaeb-128">Der Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4eaeb-128">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="4eaeb-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="4eaeb-129">-SubscriptionId</span></span>
<span data-ttu-id="4eaeb-130">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="4eaeb-130">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eaeb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eaeb-131">CommonParameters</span></span>
<span data-ttu-id="4eaeb-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eaeb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eaeb-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4eaeb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eaeb-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4eaeb-134">INPUTS</span></span>

### <span data-ttu-id="4eaeb-135">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="4eaeb-135">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="4eaeb-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4eaeb-136">OUTPUTS</span></span>

### <span data-ttu-id="4eaeb-137">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. Api20200515. IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="4eaeb-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="4eaeb-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="4eaeb-138">NOTES</span></span>

<span data-ttu-id="4eaeb-139">Aliase</span><span class="sxs-lookup"><span data-stu-id="4eaeb-139">ALIASES</span></span>

<span data-ttu-id="4eaeb-140">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4eaeb-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4eaeb-141">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4eaeb-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4eaeb-142">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="4eaeb-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4eaeb-143">Inputobject <ITimeSeriesInsightsIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="4eaeb-143">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4eaeb-144">`[AccessPolicyName <String>]`: Name der Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="4eaeb-144">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="4eaeb-145">`[EnvironmentName <String>]`: Name der Umgebung</span><span class="sxs-lookup"><span data-stu-id="4eaeb-145">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="4eaeb-146">`[EventSourceName <String>]`: Der Name der Ereignisquelle für Zeitreihen Einblicke, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4eaeb-146">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="4eaeb-147">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="4eaeb-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4eaeb-148">`[ReferenceDataSetName <String>]`: Name des referenzdatensatzes.</span><span class="sxs-lookup"><span data-stu-id="4eaeb-148">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="4eaeb-149">`[ResourceGroupName <String>]`: Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4eaeb-149">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="4eaeb-150">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="4eaeb-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="4eaeb-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4eaeb-151">RELATED LINKS</span></span>

