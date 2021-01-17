---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: b4f27c31ebc3eb54727d6df1139409529c20eed9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460547"
---
# <span data-ttu-id="a5dbb-101">New-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="a5dbb-101">New-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="a5dbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5dbb-102">SYNOPSIS</span></span>
<span data-ttu-id="a5dbb-103">Erstellen Sie eine Umgebung in der angegebenen Abonnement- und Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-103">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="a5dbb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5dbb-104">SYNTAX</span></span>

### <span data-ttu-id="a5dbb-105">Gen1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="a5dbb-105">Gen1 (Default)</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Capacity <Int32>
 -DataRetentionTime <TimeSpan> -Kind <Kind> -Location <String> -Sku <SkuName> [-SubscriptionId <String>]
 [-PartitionKeyProperty <ITimeSeriesIdProperty[]>] [-StorageLimitExceededBehavior <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a5dbb-106">Gen2</span><span class="sxs-lookup"><span data-stu-id="a5dbb-106">Gen2</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Kind <Kind> -Location <String>
 -Sku <SkuName> -StorageAccountKey <SecureString> -StorageAccountName <String>
 -TimeSeriesIdProperty <ITimeSeriesIdProperty[]> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-WarmStoreDataRetentionTime <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="a5dbb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5dbb-107">DESCRIPTION</span></span>
<span data-ttu-id="a5dbb-108">Erstellen Sie eine Umgebung in der angegebenen Abonnement- und Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-108">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="a5dbb-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a5dbb-109">EXAMPLES</span></span>

### <span data-ttu-id="a5dbb-110">Beispiel 1: Erstellen einer Insightsumgebung für Zeitreihen der Generation 1</span><span class="sxs-lookup"><span data-stu-id="a5dbb-110">Example 1: Create a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $TimeSpan = New-TimeSpan -Days 1 -Hours 1 -Minutes 25
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Kind Gen1 -Location eastus -Sku S1 -DataRetentionTime $TimeSpan -Capacity 2

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen1 eastus   tsitest001 2           S1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="a5dbb-111">Mit diesem Befehl wird eine Umgebung zum Aufblick von Zeitreihen der Generation 1 erstellt.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-111">This command creates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="a5dbb-112">Beispiel 2: Erstellen einer Insightsumgebung für Zeitreihen der Generation 2</span><span class="sxs-lookup"><span data-stu-id="a5dbb-112">Example 2: Create a Gen2 time series insights environment</span></span>
```powershell
PS C:\> $ks = Get-AzStorageAccountKey -ResourceGroupName "testgroup" -Name "staccount001"
PS C:\> $k  = $ks[0].Value | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest002 -Kind Gen2 -Location eastus -Sku L1 -StorageAccountName staccount001 -StorageAccountKey $k -TimeSeriesIdProperty @{name='cdc';type='string'}

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen2 eastus   tsitest002 1           L1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="a5dbb-113">Dieser Befehl erstellt eine Umgebung zum Aufblick von Zeitreihen der Generation 2.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-113">This command creates a Gen2 time series insights environment.</span></span>

## <span data-ttu-id="a5dbb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5dbb-114">PARAMETERS</span></span>

### <span data-ttu-id="a5dbb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5dbb-115">-AsJob</span></span>
<span data-ttu-id="a5dbb-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="a5dbb-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a5dbb-117">-Capacity</span><span class="sxs-lookup"><span data-stu-id="a5dbb-117">-Capacity</span></span>
<span data-ttu-id="a5dbb-118">Die Kapazität der SKU.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-118">The capacity of the sku.</span></span>
<span data-ttu-id="a5dbb-119">Für Umgebungen der Generation 1 kann dieser Wert geändert werden, um das Skalieren von Umgebungen nach deren Erstellen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-119">For Gen1 environments, this value can be changed to support scale out of environments after they have been created.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Gen1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5dbb-120">-DataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="a5dbb-120">-DataRetentionTime</span></span>
<span data-ttu-id="a5dbb-121">Die Datenaufbewahrungszeit.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-121">The data retention time.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Gen1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5dbb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5dbb-122">-DefaultProfile</span></span>
<span data-ttu-id="a5dbb-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5dbb-124">-Kind</span><span class="sxs-lookup"><span data-stu-id="a5dbb-124">-Kind</span></span>
<span data-ttu-id="a5dbb-125">Die Art der Umgebung.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-125">The kind of the environment.</span></span>

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

### <span data-ttu-id="a5dbb-126">-Location</span><span class="sxs-lookup"><span data-stu-id="a5dbb-126">-Location</span></span>
<span data-ttu-id="a5dbb-127">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-127">The location of the resource.</span></span>

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

### <span data-ttu-id="a5dbb-128">-Name</span><span class="sxs-lookup"><span data-stu-id="a5dbb-128">-Name</span></span>
<span data-ttu-id="a5dbb-129">Name der Umgebung</span><span class="sxs-lookup"><span data-stu-id="a5dbb-129">Name of the environment</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5dbb-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a5dbb-130">-NoWait</span></span>
<span data-ttu-id="a5dbb-131">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="a5dbb-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a5dbb-132">-PartitionKeyProperty</span><span class="sxs-lookup"><span data-stu-id="a5dbb-132">-PartitionKeyProperty</span></span>
<span data-ttu-id="a5dbb-133">Die Liste der Ereigniseigenschaften, die zum Partitionieren von Daten in der Umgebung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-133">The list of event properties which will be used to partition data in the environment.</span></span>
<span data-ttu-id="a5dbb-134">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" zu "PARTITIONKEYPROPERTY"-Eigenschaften und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-134">To construct, see NOTES section for PARTITIONKEYPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.ITimeSeriesIdProperty[]
Parameter Sets: Gen1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5dbb-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5dbb-135">-ResourceGroupName</span></span>
<span data-ttu-id="a5dbb-136">Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="a5dbb-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="a5dbb-137">-Sku</span></span>
<span data-ttu-id="a5dbb-138">Der Name dieser SKU.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-138">The name of this SKU.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5dbb-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a5dbb-139">-StorageAccountKey</span></span>
<span data-ttu-id="a5dbb-140">Der Wert des Verwaltungsschlüssels, der dem Time Series Insights-Dienst Schreibzugriff auf das Speicherkonto gewährt.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-140">The value of the management key that grants the Time Series Insights service write access to the storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5dbb-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a5dbb-141">-StorageAccountName</span></span>
<span data-ttu-id="a5dbb-142">Der Name des Speicherkontos, das die langfristigen Daten der Umgebung enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-142">The name of the storage account that will hold the environment's long term data.</span></span>

```yaml
Type: System.String
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5dbb-143">-StorageLimitExceededBehavior</span><span class="sxs-lookup"><span data-stu-id="a5dbb-143">-StorageLimitExceededBehavior</span></span>
<span data-ttu-id="a5dbb-144">Das Verhalten, das der Time Series Insights-Dienst nutzen sollte, wenn die Kapazität der Umgebung überschritten wurde</span><span class="sxs-lookup"><span data-stu-id="a5dbb-144">The behavior the Time Series Insights service should take when the environment's capacity has been exceeded</span></span>

```yaml
Type: System.String
Parameter Sets: Gen1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5dbb-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5dbb-145">-SubscriptionId</span></span>
<span data-ttu-id="a5dbb-146">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-146">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="a5dbb-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="a5dbb-147">-Tag</span></span>
<span data-ttu-id="a5dbb-148">Schlüssel-Wert-Paare zusätzlicher Eigenschaften für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-148">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="a5dbb-149">-TimeSeriesIdProperty</span><span class="sxs-lookup"><span data-stu-id="a5dbb-149">-TimeSeriesIdProperty</span></span>
<span data-ttu-id="a5dbb-150">Die Liste der Ereigniseigenschaften, die verwendet wird, um die Zeitreihen-ID der Umgebung zu definieren. Informationen zum Erstellen finden Sie im Abschnitt "NOTES" zu den #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-150">The list of event properties which will be used to define the environment's time series id. To construct, see NOTES section for TIMESERIESIDPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.ITimeSeriesIdProperty[]
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5dbb-151">-WarmStoreDataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="a5dbb-151">-WarmStoreDataRetentionTime</span></span>
<span data-ttu-id="a5dbb-152">ISO8601-Zeitraum, der die Anzahl der Tage anzahlt, für die die Ereignisse der Umgebung für die Abfrage aus dem Warmspeicher verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-152">ISO8601 timespan specifying the number of days the environment's events will be available for query from the warm store.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Gen2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5dbb-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5dbb-153">-Confirm</span></span>
<span data-ttu-id="a5dbb-154">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5dbb-155">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a5dbb-155">-WhatIf</span></span>
<span data-ttu-id="a5dbb-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5dbb-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5dbb-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5dbb-158">CommonParameters</span></span>
<span data-ttu-id="a5dbb-159">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5dbb-160">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5dbb-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5dbb-161">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a5dbb-161">INPUTS</span></span>

## <span data-ttu-id="a5dbb-162">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a5dbb-162">OUTPUTS</span></span>

### <span data-ttu-id="a5dbb-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="a5dbb-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="a5dbb-164">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a5dbb-164">NOTES</span></span>

<span data-ttu-id="a5dbb-165">ALIASE</span><span class="sxs-lookup"><span data-stu-id="a5dbb-165">ALIASES</span></span>

<span data-ttu-id="a5dbb-166">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="a5dbb-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a5dbb-167">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a5dbb-168">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a5dbb-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: Die Liste der Ereigniseigenschaften, die zum Partitionieren von Daten in der Umgebung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to partition data in the environment.</span></span>
  - <span data-ttu-id="a5dbb-170">`[Name <String>]`: Der Name der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-170">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="a5dbb-171">`[Type <PropertyType?>]`: Der Typ der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-171">`[Type <PropertyType?>]`: The type of the property.</span></span>

<span data-ttu-id="a5dbb-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: Die Liste der Ereigniseigenschaften, mit denen die Zeitreihen-ID der Umgebung definiert wird.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to define the environment's time series id.</span></span>
  - <span data-ttu-id="a5dbb-173">`[Name <String>]`: Der Name der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-173">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="a5dbb-174">`[Type <PropertyType?>]`: Der Typ der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a5dbb-174">`[Type <PropertyType?>]`: The type of the property.</span></span>

## <span data-ttu-id="a5dbb-175">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a5dbb-175">RELATED LINKS</span></span>

