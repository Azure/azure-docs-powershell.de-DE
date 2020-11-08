---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: e2b7fa000251a12e09dfd7cd345f54f967962839
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167173"
---
# <span data-ttu-id="0088f-101">Update-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="0088f-101">Update-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="0088f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0088f-102">SYNOPSIS</span></span>
<span data-ttu-id="0088f-103">Aktualisiert die Umgebung mit dem angegebenen Namen in der angegebenen Abonnement-und Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0088f-103">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="0088f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0088f-104">SYNTAX</span></span>

### <span data-ttu-id="0088f-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="0088f-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0088f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0088f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0088f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0088f-107">DESCRIPTION</span></span>
<span data-ttu-id="0088f-108">Aktualisiert die Umgebung mit dem angegebenen Namen in der angegebenen Abonnement-und Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0088f-108">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="0088f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0088f-109">EXAMPLES</span></span>

### <span data-ttu-id="0088f-110">Beispiel 1: Aktualisieren einer Gen1 Zeitreihen Einblicke-Umgebung</span><span class="sxs-lookup"><span data-stu-id="0088f-110">Example 1: Update a Gen1 time series insights environment</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Tag @{'key1'='val1'}

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
SkuCapacity                  : 5
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="0088f-111">Mit diesem Befehl wird eine Gen1 Zeitreihen Einblicke-Umgebung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0088f-111">This command updates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="0088f-112">Beispiel 2: Aktualisieren einer Gen1 Zeitreihen Einblicke-Umgebung</span><span class="sxs-lookup"><span data-stu-id="0088f-112">Example 2:  Update a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001
PS C:\> Update-AzTimeSeriesInsightsEnvironment -InputObject $env -Tag @{'key2'='val2'}

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
SkuCapacity                  : 5
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="0088f-113">Mit diesem Befehl wird eine Gen1 Zeitreihen Einblicke-Umgebung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0088f-113">This command updates a Gen1 time series insights environment.</span></span>

## <span data-ttu-id="0088f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0088f-114">PARAMETERS</span></span>

### <span data-ttu-id="0088f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0088f-115">-AsJob</span></span>
<span data-ttu-id="0088f-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="0088f-116">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0088f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0088f-117">-DefaultProfile</span></span>
<span data-ttu-id="0088f-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0088f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0088f-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0088f-119">-InputObject</span></span>
<span data-ttu-id="0088f-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="0088f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0088f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0088f-121">-Name</span></span>
<span data-ttu-id="0088f-122">Der Name der Zeitreihen Einblicke-Umgebung, die der angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0088f-122">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0088f-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="0088f-123">-NoWait</span></span>
<span data-ttu-id="0088f-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="0088f-124">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0088f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0088f-125">-ResourceGroupName</span></span>
<span data-ttu-id="0088f-126">Der Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0088f-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="0088f-127">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="0088f-127">-SubscriptionId</span></span>
<span data-ttu-id="0088f-128">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="0088f-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="0088f-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="0088f-129">-Tag</span></span>
<span data-ttu-id="0088f-130">Schlüssel-Wert-Paare zusätzlicher Eigenschaften für die Umgebung.</span><span class="sxs-lookup"><span data-stu-id="0088f-130">Key-value pairs of additional properties for the environment.</span></span>

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

### <span data-ttu-id="0088f-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0088f-131">-Confirm</span></span>
<span data-ttu-id="0088f-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0088f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0088f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0088f-133">-WhatIf</span></span>
<span data-ttu-id="0088f-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0088f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0088f-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0088f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0088f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0088f-136">CommonParameters</span></span>
<span data-ttu-id="0088f-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0088f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0088f-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0088f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0088f-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0088f-139">INPUTS</span></span>

### <span data-ttu-id="0088f-140">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="0088f-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="0088f-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0088f-141">OUTPUTS</span></span>

### <span data-ttu-id="0088f-142">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. Api20200515. IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="0088f-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="0088f-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="0088f-143">NOTES</span></span>

<span data-ttu-id="0088f-144">Aliase</span><span class="sxs-lookup"><span data-stu-id="0088f-144">ALIASES</span></span>

<span data-ttu-id="0088f-145">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0088f-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0088f-146">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0088f-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0088f-147">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="0088f-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0088f-148">Inputobject <ITimeSeriesInsightsIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="0088f-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0088f-149">`[AccessPolicyName <String>]`: Name der Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="0088f-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="0088f-150">`[EnvironmentName <String>]`: Name der Umgebung</span><span class="sxs-lookup"><span data-stu-id="0088f-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="0088f-151">`[EventSourceName <String>]`: Der Name der Ereignisquelle für Zeitreihen Einblicke, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0088f-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="0088f-152">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="0088f-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0088f-153">`[ReferenceDataSetName <String>]`: Name des referenzdatensatzes.</span><span class="sxs-lookup"><span data-stu-id="0088f-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="0088f-154">`[ResourceGroupName <String>]`: Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0088f-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="0088f-155">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="0088f-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="0088f-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0088f-156">RELATED LINKS</span></span>

