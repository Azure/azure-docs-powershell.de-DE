---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 151b8a431183727dbfaec242705421ba775b0b99
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948192"
---
# <span data-ttu-id="14e47-101">Get-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="14e47-101">Get-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="14e47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14e47-102">SYNOPSIS</span></span>
<span data-ttu-id="14e47-103">Ruft die Umgebung mit dem angegebenen Namen in der angegebenen Abonnement- und Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="14e47-103">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="14e47-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14e47-104">SYNTAX</span></span>

### <span data-ttu-id="14e47-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="14e47-105">List1 (Default)</span></span>
```
Get-AzTimeSeriesInsightsEnvironment [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="14e47-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="14e47-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="14e47-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="14e47-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="14e47-108">Liste</span><span class="sxs-lookup"><span data-stu-id="14e47-108">List</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="14e47-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="14e47-109">DESCRIPTION</span></span>
<span data-ttu-id="14e47-110">Ruft die Umgebung mit dem angegebenen Namen in der angegebenen Abonnement- und Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="14e47-110">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="14e47-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="14e47-111">EXAMPLES</span></span>

### <span data-ttu-id="14e47-112">Beispiel 1: Erhalten einer Umgebung für Einblicke in Zeitreihen</span><span class="sxs-lookup"><span data-stu-id="14e47-112">Example 1: Get a time series insights environment</span></span>
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

<span data-ttu-id="14e47-113">Dieser Befehl ruft eine Umgebung für Zeitreiheneinblicke ab.</span><span class="sxs-lookup"><span data-stu-id="14e47-113">This command gets a time series insights environment.</span></span>

### <span data-ttu-id="14e47-114">Beispiel 2: Listen aller Zeitreiheneinblickumgebungen</span><span class="sxs-lookup"><span data-stu-id="14e47-114">Example 2: List all time series insights environments</span></span>
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

<span data-ttu-id="14e47-115">Mit diesem Befehl werden alle Zeitreiheneinblickumgebungen in einer Ressourcengruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="14e47-115">This command lists all time series insights environments in a resource group.</span></span>

### <span data-ttu-id="14e47-116">Beispiel 3: Erhalten einer Umgebung für Zeitreiheneinblicke nach Objekt</span><span class="sxs-lookup"><span data-stu-id="14e47-116">Example 3: Get a time series insights environment by object</span></span>
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

<span data-ttu-id="14e47-117">Dieser Befehl ruft eine Zeitreiheneinblickumgebung ab.</span><span class="sxs-lookup"><span data-stu-id="14e47-117">This command gets a time series insights environments.</span></span>

## <span data-ttu-id="14e47-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="14e47-118">PARAMETERS</span></span>

### <span data-ttu-id="14e47-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14e47-119">-DefaultProfile</span></span>
<span data-ttu-id="14e47-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14e47-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14e47-121">-Erweitern</span><span class="sxs-lookup"><span data-stu-id="14e47-121">-Expand</span></span>
<span data-ttu-id="14e47-122">Das $expand=status enthält den Status der internen Dienste der Umgebung im Dienst Zeitreiheneinblicke.</span><span class="sxs-lookup"><span data-stu-id="14e47-122">Setting $expand=status will include the status of the internal services of the environment in the Time Series Insights service.</span></span>

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

### <span data-ttu-id="14e47-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14e47-123">-InputObject</span></span>
<span data-ttu-id="14e47-124">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="14e47-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="14e47-125">-Name</span><span class="sxs-lookup"><span data-stu-id="14e47-125">-Name</span></span>
<span data-ttu-id="14e47-126">Der Name der Zeitreiheneinblickumgebung, die der angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="14e47-126">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="14e47-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14e47-127">-ResourceGroupName</span></span>
<span data-ttu-id="14e47-128">Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="14e47-128">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="14e47-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="14e47-129">-SubscriptionId</span></span>
<span data-ttu-id="14e47-130">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="14e47-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="14e47-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14e47-131">CommonParameters</span></span>
<span data-ttu-id="14e47-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14e47-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14e47-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14e47-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14e47-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="14e47-134">INPUTS</span></span>

### <span data-ttu-id="14e47-135">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="14e47-135">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="14e47-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="14e47-136">OUTPUTS</span></span>

### <span data-ttu-id="14e47-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="14e47-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="14e47-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="14e47-138">NOTES</span></span>

<span data-ttu-id="14e47-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="14e47-139">ALIASES</span></span>

<span data-ttu-id="14e47-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="14e47-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="14e47-141">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="14e47-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="14e47-142">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="14e47-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="14e47-143">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="14e47-143">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="14e47-144">`[AccessPolicyName <String>]`: Name der Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="14e47-144">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="14e47-145">`[EnvironmentName <String>]`: Name der Umgebung</span><span class="sxs-lookup"><span data-stu-id="14e47-145">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="14e47-146">`[EventSourceName <String>]`: Der Name der Time Series Insights-Ereignisquelle, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="14e47-146">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="14e47-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="14e47-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="14e47-148">`[ReferenceDataSetName <String>]`: Name des Bezugsdatensets.</span><span class="sxs-lookup"><span data-stu-id="14e47-148">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="14e47-149">`[ResourceGroupName <String>]`: Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="14e47-149">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="14e47-150">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="14e47-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="14e47-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="14e47-151">RELATED LINKS</span></span>

