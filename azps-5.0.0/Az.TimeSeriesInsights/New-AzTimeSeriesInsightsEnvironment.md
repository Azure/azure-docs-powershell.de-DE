---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: b4f27c31ebc3eb54727d6df1139409529c20eed9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178657"
---
# <span data-ttu-id="b48e5-101">New-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="b48e5-101">New-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="b48e5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b48e5-102">SYNOPSIS</span></span>
<span data-ttu-id="b48e5-103">Erstellen Sie eine Umgebung in der angegebenen Abonnement-und Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b48e5-103">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="b48e5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b48e5-104">SYNTAX</span></span>

### <span data-ttu-id="b48e5-105">Gen1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="b48e5-105">Gen1 (Default)</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Capacity <Int32>
 -DataRetentionTime <TimeSpan> -Kind <Kind> -Location <String> -Sku <SkuName> [-SubscriptionId <String>]
 [-PartitionKeyProperty <ITimeSeriesIdProperty[]>] [-StorageLimitExceededBehavior <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b48e5-106">Gen2</span><span class="sxs-lookup"><span data-stu-id="b48e5-106">Gen2</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Kind <Kind> -Location <String>
 -Sku <SkuName> -StorageAccountKey <SecureString> -StorageAccountName <String>
 -TimeSeriesIdProperty <ITimeSeriesIdProperty[]> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-WarmStoreDataRetentionTime <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b48e5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b48e5-107">DESCRIPTION</span></span>
<span data-ttu-id="b48e5-108">Erstellen Sie eine Umgebung in der angegebenen Abonnement-und Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b48e5-108">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="b48e5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b48e5-109">EXAMPLES</span></span>

### <span data-ttu-id="b48e5-110">Beispiel 1: Erstellen einer Gen1-Umgebung für Zeitreihen</span><span class="sxs-lookup"><span data-stu-id="b48e5-110">Example 1: Create a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $TimeSpan = New-TimeSpan -Days 1 -Hours 1 -Minutes 25
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Kind Gen1 -Location eastus -Sku S1 -DataRetentionTime $TimeSpan -Capacity 2

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen1 eastus   tsitest001 2           S1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="b48e5-111">Mit diesem Befehl wird eine Gen1 Zeitreihen Einblicke-Umgebung erstellt.</span><span class="sxs-lookup"><span data-stu-id="b48e5-111">This command creates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="b48e5-112">Beispiel 2: Erstellen einer Gen2-Umgebung für Zeitreihen</span><span class="sxs-lookup"><span data-stu-id="b48e5-112">Example 2: Create a Gen2 time series insights environment</span></span>
```powershell
PS C:\> $ks = Get-AzStorageAccountKey -ResourceGroupName "testgroup" -Name "staccount001"
PS C:\> $k  = $ks[0].Value | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest002 -Kind Gen2 -Location eastus -Sku L1 -StorageAccountName staccount001 -StorageAccountKey $k -TimeSeriesIdProperty @{name='cdc';type='string'}

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen2 eastus   tsitest002 1           L1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="b48e5-113">Mit diesem Befehl wird eine Gen2 Zeitreihen Einblicke-Umgebung erstellt.</span><span class="sxs-lookup"><span data-stu-id="b48e5-113">This command creates a Gen2 time series insights environment.</span></span>

## <span data-ttu-id="b48e5-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b48e5-114">PARAMETERS</span></span>

### <span data-ttu-id="b48e5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b48e5-115">-AsJob</span></span>
<span data-ttu-id="b48e5-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="b48e5-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b48e5-117">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="b48e5-117">-Capacity</span></span>
<span data-ttu-id="b48e5-118">Die Kapazität der SKU.</span><span class="sxs-lookup"><span data-stu-id="b48e5-118">The capacity of the sku.</span></span>
<span data-ttu-id="b48e5-119">Bei Gen1-Umgebungen kann dieser Wert so geändert werden, dass der Skalierungsfaktor außerhalb der Umgebungen nach der Erstellung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b48e5-119">For Gen1 environments, this value can be changed to support scale out of environments after they have been created.</span></span>

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

### <span data-ttu-id="b48e5-120">-Dataretentions Zeit</span><span class="sxs-lookup"><span data-stu-id="b48e5-120">-DataRetentionTime</span></span>
<span data-ttu-id="b48e5-121">Die Daten Aufbewahrungszeit.</span><span class="sxs-lookup"><span data-stu-id="b48e5-121">The data retention time.</span></span>

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

### <span data-ttu-id="b48e5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b48e5-122">-DefaultProfile</span></span>
<span data-ttu-id="b48e5-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b48e5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b48e5-124">-Art</span><span class="sxs-lookup"><span data-stu-id="b48e5-124">-Kind</span></span>
<span data-ttu-id="b48e5-125">Die Art der Umgebung.</span><span class="sxs-lookup"><span data-stu-id="b48e5-125">The kind of the environment.</span></span>

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

### <span data-ttu-id="b48e5-126">-Standort</span><span class="sxs-lookup"><span data-stu-id="b48e5-126">-Location</span></span>
<span data-ttu-id="b48e5-127">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="b48e5-127">The location of the resource.</span></span>

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

### <span data-ttu-id="b48e5-128">-Name</span><span class="sxs-lookup"><span data-stu-id="b48e5-128">-Name</span></span>
<span data-ttu-id="b48e5-129">Name der Umgebung</span><span class="sxs-lookup"><span data-stu-id="b48e5-129">Name of the environment</span></span>

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

### <span data-ttu-id="b48e5-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b48e5-130">-NoWait</span></span>
<span data-ttu-id="b48e5-131">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="b48e5-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b48e5-132">-PartitionKeyProperty</span><span class="sxs-lookup"><span data-stu-id="b48e5-132">-PartitionKeyProperty</span></span>
<span data-ttu-id="b48e5-133">Die Liste der Ereigniseigenschaften, die zum Partitionieren von Daten in der Umgebung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b48e5-133">The list of event properties which will be used to partition data in the environment.</span></span>
<span data-ttu-id="b48e5-134">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für PARTITIONKEYPROPERTY-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="b48e5-134">To construct, see NOTES section for PARTITIONKEYPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="b48e5-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b48e5-135">-ResourceGroupName</span></span>
<span data-ttu-id="b48e5-136">Der Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b48e5-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="b48e5-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="b48e5-137">-Sku</span></span>
<span data-ttu-id="b48e5-138">Der Name dieser SKU.</span><span class="sxs-lookup"><span data-stu-id="b48e5-138">The name of this SKU.</span></span>

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

### <span data-ttu-id="b48e5-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="b48e5-139">-StorageAccountKey</span></span>
<span data-ttu-id="b48e5-140">Der Wert des Verwaltungs Schlüssels, der dem Zeitreihen Insights-Dienst Schreibzugriff auf das Speicherkonto gewährt.</span><span class="sxs-lookup"><span data-stu-id="b48e5-140">The value of the management key that grants the Time Series Insights service write access to the storage account.</span></span>

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

### <span data-ttu-id="b48e5-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b48e5-141">-StorageAccountName</span></span>
<span data-ttu-id="b48e5-142">Der Name des speicherkontos, in dem die langfristigen Daten der Umgebung gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="b48e5-142">The name of the storage account that will hold the environment's long term data.</span></span>

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

### <span data-ttu-id="b48e5-143">-StorageLimitExceededBehavior</span><span class="sxs-lookup"><span data-stu-id="b48e5-143">-StorageLimitExceededBehavior</span></span>
<span data-ttu-id="b48e5-144">Das Verhalten, das der Zeitreihen Einblicke-Dienst ausführen sollte, wenn die Kapazität der Umgebung überschritten wurde</span><span class="sxs-lookup"><span data-stu-id="b48e5-144">The behavior the Time Series Insights service should take when the environment's capacity has been exceeded</span></span>

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

### <span data-ttu-id="b48e5-145">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="b48e5-145">-SubscriptionId</span></span>
<span data-ttu-id="b48e5-146">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="b48e5-146">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="b48e5-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="b48e5-147">-Tag</span></span>
<span data-ttu-id="b48e5-148">Schlüssel-Wert-Paare zusätzlicher Eigenschaften für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="b48e5-148">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="b48e5-149">-TimeSeriesIdProperty</span><span class="sxs-lookup"><span data-stu-id="b48e5-149">-TimeSeriesIdProperty</span></span>
<span data-ttu-id="b48e5-150">Die Liste der Ereigniseigenschaften, die verwendet werden, um die Zeitreihen-ID der Umgebung zu definieren. Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für TIMESERIESIDPROPERTY-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="b48e5-150">The list of event properties which will be used to define the environment's time series id. To construct, see NOTES section for TIMESERIESIDPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="b48e5-151">-WarmStoreDataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="b48e5-151">-WarmStoreDataRetentionTime</span></span>
<span data-ttu-id="b48e5-152">ISO8601-TimeSpan, die die Anzahl der Tage angibt, die die Ereignisse der Umgebung für Abfragen aus dem warmen Store verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b48e5-152">ISO8601 timespan specifying the number of days the environment's events will be available for query from the warm store.</span></span>

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

### <span data-ttu-id="b48e5-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b48e5-153">-Confirm</span></span>
<span data-ttu-id="b48e5-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b48e5-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b48e5-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b48e5-155">-WhatIf</span></span>
<span data-ttu-id="b48e5-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b48e5-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b48e5-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b48e5-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b48e5-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b48e5-158">CommonParameters</span></span>
<span data-ttu-id="b48e5-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b48e5-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b48e5-160">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b48e5-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b48e5-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b48e5-161">INPUTS</span></span>

## <span data-ttu-id="b48e5-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b48e5-162">OUTPUTS</span></span>

### <span data-ttu-id="b48e5-163">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. Api20200515. IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="b48e5-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="b48e5-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="b48e5-164">NOTES</span></span>

<span data-ttu-id="b48e5-165">Aliase</span><span class="sxs-lookup"><span data-stu-id="b48e5-165">ALIASES</span></span>

<span data-ttu-id="b48e5-166">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b48e5-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b48e5-167">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b48e5-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b48e5-168">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="b48e5-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b48e5-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty [] >: die Liste der Ereigniseigenschaften, die zum Partitionieren von Daten in der Umgebung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b48e5-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to partition data in the environment.</span></span>
  - <span data-ttu-id="b48e5-170">`[Name <String>]`: Der Name der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b48e5-170">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="b48e5-171">`[Type <PropertyType?>]`: Der Typ der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b48e5-171">`[Type <PropertyType?>]`: The type of the property.</span></span>

<span data-ttu-id="b48e5-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty [] >: die Liste der Ereigniseigenschaften, die verwendet werden, um die Zeitreihen-ID der Umgebung zu definieren.</span><span class="sxs-lookup"><span data-stu-id="b48e5-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to define the environment's time series id.</span></span>
  - <span data-ttu-id="b48e5-173">`[Name <String>]`: Der Name der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b48e5-173">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="b48e5-174">`[Type <PropertyType?>]`: Der Typ der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b48e5-174">`[Type <PropertyType?>]`: The type of the property.</span></span>

## <span data-ttu-id="b48e5-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b48e5-175">RELATED LINKS</span></span>

