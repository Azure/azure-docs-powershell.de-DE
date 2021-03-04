---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 51cbe7cd6d4e08543feadb5ddd096330763b7236
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920139"
---
# <span data-ttu-id="79f37-101">New-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="79f37-101">New-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="79f37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79f37-102">SYNOPSIS</span></span>
<span data-ttu-id="79f37-103">Erstellen Sie eine Umgebung in der angegebenen Abonnement- und Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="79f37-103">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="79f37-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79f37-104">SYNTAX</span></span>

### <span data-ttu-id="79f37-105">Gen1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="79f37-105">Gen1 (Default)</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Capacity <Int32>
 -DataRetentionTime <TimeSpan> -Kind <Kind> -Location <String> -Sku <SkuName> [-SubscriptionId <String>]
 [-PartitionKeyProperty <ITimeSeriesIdProperty[]>] [-StorageLimitExceededBehavior <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="79f37-106">Gen2</span><span class="sxs-lookup"><span data-stu-id="79f37-106">Gen2</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Kind <Kind> -Location <String>
 -Sku <SkuName> -StorageAccountKey <SecureString> -StorageAccountName <String>
 -TimeSeriesIdProperty <ITimeSeriesIdProperty[]> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-WarmStoreDataRetentionTime <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="79f37-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79f37-107">DESCRIPTION</span></span>
<span data-ttu-id="79f37-108">Erstellen Sie eine Umgebung in der angegebenen Abonnement- und Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="79f37-108">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="79f37-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="79f37-109">EXAMPLES</span></span>

### <span data-ttu-id="79f37-110">Beispiel 1: Erstellen einer Umgebung für Gen1-Zeitreiheneinblicke</span><span class="sxs-lookup"><span data-stu-id="79f37-110">Example 1: Create a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $TimeSpan = New-TimeSpan -Days 1 -Hours 1 -Minutes 25
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Kind Gen1 -Location eastus -Sku S1 -DataRetentionTime $TimeSpan -Capacity 2

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen1 eastus   tsitest001 2           S1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="79f37-111">Mit diesem Befehl wird eine Gen1-Zeitreiheneinblickumgebung erstellt.</span><span class="sxs-lookup"><span data-stu-id="79f37-111">This command creates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="79f37-112">Beispiel 2: Erstellen einer Gen2-Zeitreiheneinblickumgebung</span><span class="sxs-lookup"><span data-stu-id="79f37-112">Example 2: Create a Gen2 time series insights environment</span></span>
```powershell
PS C:\> $ks = Get-AzStorageAccountKey -ResourceGroupName "testgroup" -Name "staccount001"
PS C:\> $k  = $ks[0].Value | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest002 -Kind Gen2 -Location eastus -Sku L1 -StorageAccountName staccount001 -StorageAccountKey $k -TimeSeriesIdProperty @{name='cdc';type='string'}

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen2 eastus   tsitest002 1           L1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="79f37-113">Mit diesem Befehl wird eine Gen2-Zeitreiheneinblickumgebung erstellt.</span><span class="sxs-lookup"><span data-stu-id="79f37-113">This command creates a Gen2 time series insights environment.</span></span>

## <span data-ttu-id="79f37-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="79f37-114">PARAMETERS</span></span>

### <span data-ttu-id="79f37-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79f37-115">-AsJob</span></span>
<span data-ttu-id="79f37-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="79f37-116">Run the command as a job</span></span>

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

### <span data-ttu-id="79f37-117">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="79f37-117">-Capacity</span></span>
<span data-ttu-id="79f37-118">Die Kapazität der Sku.</span><span class="sxs-lookup"><span data-stu-id="79f37-118">The capacity of the sku.</span></span>
<span data-ttu-id="79f37-119">Für Gen1-Umgebungen kann dieser Wert geändert werden, um skalierungs-out von Umgebungen zu unterstützen, nachdem sie erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="79f37-119">For Gen1 environments, this value can be changed to support scale out of environments after they have been created.</span></span>

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

### <span data-ttu-id="79f37-120">-DataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="79f37-120">-DataRetentionTime</span></span>
<span data-ttu-id="79f37-121">Die Aufbewahrungszeit für Daten.</span><span class="sxs-lookup"><span data-stu-id="79f37-121">The data retention time.</span></span>

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

### <span data-ttu-id="79f37-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79f37-122">-DefaultProfile</span></span>
<span data-ttu-id="79f37-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79f37-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79f37-124">-Kind</span><span class="sxs-lookup"><span data-stu-id="79f37-124">-Kind</span></span>
<span data-ttu-id="79f37-125">Die Art der Umgebung.</span><span class="sxs-lookup"><span data-stu-id="79f37-125">The kind of the environment.</span></span>

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

### <span data-ttu-id="79f37-126">-Location</span><span class="sxs-lookup"><span data-stu-id="79f37-126">-Location</span></span>
<span data-ttu-id="79f37-127">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="79f37-127">The location of the resource.</span></span>

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

### <span data-ttu-id="79f37-128">-Name</span><span class="sxs-lookup"><span data-stu-id="79f37-128">-Name</span></span>
<span data-ttu-id="79f37-129">Name der Umgebung</span><span class="sxs-lookup"><span data-stu-id="79f37-129">Name of the environment</span></span>

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

### <span data-ttu-id="79f37-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="79f37-130">-NoWait</span></span>
<span data-ttu-id="79f37-131">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="79f37-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="79f37-132">-PartitionKeyProperty</span><span class="sxs-lookup"><span data-stu-id="79f37-132">-PartitionKeyProperty</span></span>
<span data-ttu-id="79f37-133">Die Liste der Ereigniseigenschaften, die zum Partitionieren von Daten in der Umgebung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79f37-133">The list of event properties which will be used to partition data in the environment.</span></span>
<span data-ttu-id="79f37-134">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu PARTITIONKEYPROPERTY-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="79f37-134">To construct, see NOTES section for PARTITIONKEYPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="79f37-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79f37-135">-ResourceGroupName</span></span>
<span data-ttu-id="79f37-136">Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="79f37-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="79f37-137">-Sku</span><span class="sxs-lookup"><span data-stu-id="79f37-137">-Sku</span></span>
<span data-ttu-id="79f37-138">Der Name dieser SKU.</span><span class="sxs-lookup"><span data-stu-id="79f37-138">The name of this SKU.</span></span>

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

### <span data-ttu-id="79f37-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="79f37-139">-StorageAccountKey</span></span>
<span data-ttu-id="79f37-140">Der Wert des Verwaltungsschlüssels, der dem Dienst Zeitreiheneinblicke Schreibzugriff auf das Speicherkonto gewährt.</span><span class="sxs-lookup"><span data-stu-id="79f37-140">The value of the management key that grants the Time Series Insights service write access to the storage account.</span></span>

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

### <span data-ttu-id="79f37-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="79f37-141">-StorageAccountName</span></span>
<span data-ttu-id="79f37-142">Der Name des Speicherkontos, das die langfristigen Daten der Umgebung enthält.</span><span class="sxs-lookup"><span data-stu-id="79f37-142">The name of the storage account that will hold the environment's long term data.</span></span>

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

### <span data-ttu-id="79f37-143">-StorageLimitExceededBehavior</span><span class="sxs-lookup"><span data-stu-id="79f37-143">-StorageLimitExceededBehavior</span></span>
<span data-ttu-id="79f37-144">Das Verhalten, das der Dienst "Zeitreiheneinblicke" übernehmen sollte, wenn die Kapazität der Umgebung überschritten wurde</span><span class="sxs-lookup"><span data-stu-id="79f37-144">The behavior the Time Series Insights service should take when the environment's capacity has been exceeded</span></span>

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

### <span data-ttu-id="79f37-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="79f37-145">-SubscriptionId</span></span>
<span data-ttu-id="79f37-146">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="79f37-146">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="79f37-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="79f37-147">-Tag</span></span>
<span data-ttu-id="79f37-148">Schlüssel-Wert-Paare zusätzlicher Eigenschaften für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="79f37-148">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="79f37-149">-TimeSeriesIdProperty</span><span class="sxs-lookup"><span data-stu-id="79f37-149">-TimeSeriesIdProperty</span></span>
<span data-ttu-id="79f37-150">Die Liste der Ereigniseigenschaften, die zum Definieren der Zeitreihen-ID der Umgebung verwendet werden. Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu den Eigenschaften von TIMESERIESIDPROPERTY, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="79f37-150">The list of event properties which will be used to define the environment's time series id. To construct, see NOTES section for TIMESERIESIDPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="79f37-151">-WarmStoreDataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="79f37-151">-WarmStoreDataRetentionTime</span></span>
<span data-ttu-id="79f37-152">ISO8601-Zeitspanne, die die Anzahl der Tage an gibt, in der die Ereignisse der Umgebung für abfragen aus dem warm store verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="79f37-152">ISO8601 timespan specifying the number of days the environment's events will be available for query from the warm store.</span></span>

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

### <span data-ttu-id="79f37-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="79f37-153">-Confirm</span></span>
<span data-ttu-id="79f37-154">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="79f37-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79f37-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79f37-155">-WhatIf</span></span>
<span data-ttu-id="79f37-156">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="79f37-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79f37-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="79f37-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79f37-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79f37-158">CommonParameters</span></span>
<span data-ttu-id="79f37-159">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79f37-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79f37-160">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79f37-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79f37-161">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="79f37-161">INPUTS</span></span>

## <span data-ttu-id="79f37-162">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="79f37-162">OUTPUTS</span></span>

### <span data-ttu-id="79f37-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="79f37-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="79f37-164">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="79f37-164">NOTES</span></span>

<span data-ttu-id="79f37-165">ALIASE</span><span class="sxs-lookup"><span data-stu-id="79f37-165">ALIASES</span></span>

<span data-ttu-id="79f37-166">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="79f37-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="79f37-167">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="79f37-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="79f37-168">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="79f37-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="79f37-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: Die Liste der Ereigniseigenschaften, die zum Partitionieren von Daten in der Umgebung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79f37-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to partition data in the environment.</span></span>
  - <span data-ttu-id="79f37-170">`[Name <String>]`: Der Name der -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="79f37-170">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="79f37-171">`[Type <PropertyType?>]`: Der Typ der -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="79f37-171">`[Type <PropertyType?>]`: The type of the property.</span></span>

<span data-ttu-id="79f37-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: Die Liste der Ereigniseigenschaften, die zum Definieren der Zeitreihen-ID der Umgebung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79f37-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to define the environment's time series id.</span></span>
  - <span data-ttu-id="79f37-173">`[Name <String>]`: Der Name der -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="79f37-173">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="79f37-174">`[Type <PropertyType?>]`: Der Typ der -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="79f37-174">`[Type <PropertyType?>]`: The type of the property.</span></span>

## <span data-ttu-id="79f37-175">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="79f37-175">RELATED LINKS</span></span>

