---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175610"
---
# <span data-ttu-id="c1be5-101">Update-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="c1be5-101">Update-AzFunctionAppPlan</span></span>

## <span data-ttu-id="c1be5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c1be5-102">SYNOPSIS</span></span>
<span data-ttu-id="c1be5-103">Aktualisiert einen Funktions-APP-Service Plan.</span><span class="sxs-lookup"><span data-stu-id="c1be5-103">Updates a function app service plan.</span></span>

## <span data-ttu-id="c1be5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1be5-104">SYNTAX</span></span>

### <span data-ttu-id="c1be5-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c1be5-105">ByName (Default)</span></span>
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c1be5-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="c1be5-106">ByObjectInput</span></span>
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c1be5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1be5-107">DESCRIPTION</span></span>
<span data-ttu-id="c1be5-108">Aktualisiert einen Funktions-APP-Service Plan.</span><span class="sxs-lookup"><span data-stu-id="c1be5-108">Updates a function app service plan.</span></span>

## <span data-ttu-id="c1be5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c1be5-109">EXAMPLES</span></span>

### <span data-ttu-id="c1be5-110">Beispiel 1: Aktualisieren eines App-Service-Plans auf ep2 SKU mit maximal zwanzig Mitarbeitern.</span><span class="sxs-lookup"><span data-stu-id="c1be5-110">Example 1: Update an app service plan to EP2 sku with twenty maximum workers.</span></span>
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

<span data-ttu-id="c1be5-111">Mit diesem Befehl wird ein App-Service Plan auf ep2 SKU mit zwanzig maximalen Arbeitskräften aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c1be5-111">This command updates an app service plan to EP2 sku with twenty maximum workers.</span></span>

## <span data-ttu-id="c1be5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1be5-112">PARAMETERS</span></span>

### <span data-ttu-id="c1be5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1be5-113">-AsJob</span></span>
<span data-ttu-id="c1be5-114">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="c1be5-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="c1be5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1be5-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="c1be5-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c1be5-116">-InputObject</span></span>
<span data-ttu-id="c1be5-117">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c1be5-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1be5-118">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="c1be5-118">-MaximumWorkerCount</span></span>
<span data-ttu-id="c1be5-119">Die maximale Anzahl von Arbeitskräften für den App-Service Plan.</span><span class="sxs-lookup"><span data-stu-id="c1be5-119">The maximum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1be5-120">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="c1be5-120">-MinimumWorkerCount</span></span>
<span data-ttu-id="c1be5-121">Die Mindestanzahl von Arbeitskräften für den App-Service Plan.</span><span class="sxs-lookup"><span data-stu-id="c1be5-121">The minimum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1be5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c1be5-122">-Name</span></span>
<span data-ttu-id="c1be5-123">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="c1be5-123">Name of the App Service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1be5-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c1be5-124">-NoWait</span></span>
<span data-ttu-id="c1be5-125">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="c1be5-125">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="c1be5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1be5-126">-ResourceGroupName</span></span>
<span data-ttu-id="c1be5-127">Der Name der Ressourcengruppe, zu der die Ressource gehört.</span><span class="sxs-lookup"><span data-stu-id="c1be5-127">Name of the resource group to which the resource belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1be5-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="c1be5-128">-Sku</span></span>
<span data-ttu-id="c1be5-129">Die Plan-SKU.</span><span class="sxs-lookup"><span data-stu-id="c1be5-129">The plan sku.</span></span>
<span data-ttu-id="c1be5-130">Gültige Eingaben sind: EP1, ep2, EP3</span><span class="sxs-lookup"><span data-stu-id="c1be5-130">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="c1be5-131">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="c1be5-131">-SubscriptionId</span></span>
<span data-ttu-id="c1be5-132">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="c1be5-132">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1be5-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="c1be5-133">-Tag</span></span>
<span data-ttu-id="c1be5-134">Ressourcenkategorien.</span><span class="sxs-lookup"><span data-stu-id="c1be5-134">Resource tags.</span></span>

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

### <span data-ttu-id="c1be5-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c1be5-135">-Confirm</span></span>
<span data-ttu-id="c1be5-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c1be5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1be5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1be5-137">-WhatIf</span></span>
<span data-ttu-id="c1be5-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c1be5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1be5-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1be5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1be5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1be5-140">CommonParameters</span></span>
<span data-ttu-id="c1be5-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1be5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1be5-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1be5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1be5-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c1be5-143">INPUTS</span></span>

### <span data-ttu-id="c1be5-144">Microsoft. Azure. PowerShell. Cmdlets. Functions. Models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c1be5-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="c1be5-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c1be5-145">OUTPUTS</span></span>

### <span data-ttu-id="c1be5-146">Microsoft. Azure. PowerShell. Cmdlets. Functions. Models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c1be5-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="c1be5-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="c1be5-147">NOTES</span></span>

<span data-ttu-id="c1be5-148">Aliase</span><span class="sxs-lookup"><span data-stu-id="c1be5-148">ALIASES</span></span>

<span data-ttu-id="c1be5-149">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c1be5-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c1be5-150">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c1be5-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c1be5-151">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="c1be5-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c1be5-152">Inputobject <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="c1be5-152">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="c1be5-153">`Location <String>`: Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="c1be5-153">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="c1be5-154">`[Kind <String>]`: Art der Ressource.</span><span class="sxs-lookup"><span data-stu-id="c1be5-154">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="c1be5-155">`[Tag <IResourceTags>]`: Ressourcenkategorien.</span><span class="sxs-lookup"><span data-stu-id="c1be5-155">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="c1be5-156">`[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c1be5-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="c1be5-157">`[Capacity <Int32?>]`: Aktuelle Anzahl der Instanzen, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c1be5-157">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="c1be5-158">`[FreeOfferExpirationTime <DateTime?>]`: Der Zeitpunkt, zu dem das ﻿kostenlose Angebot der Serverfarm abläuft.</span><span class="sxs-lookup"><span data-stu-id="c1be5-158">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="c1be5-159">`[HostingEnvironmentProfileId <String>]`: Ressourcen-ID der APP-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="c1be5-159">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="c1be5-160">`[HyperV <Boolean?>]`: Wenn der Hyper-V-Container-App-Service Plan <code>true</code> , <code>false</code> andernfalls.</span><span class="sxs-lookup"><span data-stu-id="c1be5-160">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="c1be5-161">`[IsSpot <Boolean?>]`: Wenn <code>true</code> dieser APP-Service Plan über Spot-Instances verfügt.</span><span class="sxs-lookup"><span data-stu-id="c1be5-161">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="c1be5-162">`[IsXenon <Boolean?>]`: Veraltet: Wenn der Hyper-V-Container-App-Service Plan <code>true</code> , <code>false</code> andernfalls.</span><span class="sxs-lookup"><span data-stu-id="c1be5-162">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="c1be5-163">`[MaximumElasticWorkerCount <Int32?>]`: Maximale Anzahl der insgesamt für diesen ElasticScaleEnabled-App-Service Plan zulässigen Arbeitskräfte</span><span class="sxs-lookup"><span data-stu-id="c1be5-163">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="c1be5-164">`[PerSiteScaling <Boolean?>]`: Wenn <code>true</code> apps, die diesem app-Service Plan zugewiesen sind, unabhängig voneinander skaliert werden können.</span><span class="sxs-lookup"><span data-stu-id="c1be5-164">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="c1be5-165">Wenn <code>false</code> die diesem app-Service Plan zugewiesenen apps auf alle Instanzen des Plans skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="c1be5-165">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="c1be5-166">`[Reserved <Boolean?>]`: Wenn der Linux-APP <code>true</code> -Service Plan, <code>false</code> andernfalls.</span><span class="sxs-lookup"><span data-stu-id="c1be5-166">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="c1be5-167">`[SkuCapability <ICapability[]>]`: Funktionen der SKU, beispielsweise ist Traffic Manager aktiviert?</span><span class="sxs-lookup"><span data-stu-id="c1be5-167">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="c1be5-168">`[Name <String>]`: Name der SKU-Funktion.</span><span class="sxs-lookup"><span data-stu-id="c1be5-168">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="c1be5-169">`[Reason <String>]`: Grund für die SKU-Funktion.</span><span class="sxs-lookup"><span data-stu-id="c1be5-169">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="c1be5-170">`[Value <String>]`: Wert der SKU-Funktion.</span><span class="sxs-lookup"><span data-stu-id="c1be5-170">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="c1be5-171">`[SkuCapacityDefault <Int32?>]`: Standardanzahl von Arbeitskräften für diese APP-Service Plan-SKU.</span><span class="sxs-lookup"><span data-stu-id="c1be5-171">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="c1be5-172">`[SkuCapacityMaximum <Int32?>]`: Maximale Anzahl von Arbeitskräften für diese APP-Service Plan-SKU.</span><span class="sxs-lookup"><span data-stu-id="c1be5-172">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="c1be5-173">`[SkuCapacityMinimum <Int32?>]`: Mindestanzahl von Arbeitskräften für diese APP-Service Plan-SKU.</span><span class="sxs-lookup"><span data-stu-id="c1be5-173">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="c1be5-174">`[SkuCapacityScaleType <String>]`: Verfügbare Skalierungs Konfigurationen für einen app-Service Plan.</span><span class="sxs-lookup"><span data-stu-id="c1be5-174">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="c1be5-175">`[SkuFamily <String>]`: Familiencode der Ressourcen-SKU.</span><span class="sxs-lookup"><span data-stu-id="c1be5-175">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="c1be5-176">`[SkuLocation <String[]>]`: Speicherorte der SKU.</span><span class="sxs-lookup"><span data-stu-id="c1be5-176">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="c1be5-177">`[SkuName <String>]`: Name der Ressourcen-SKU.</span><span class="sxs-lookup"><span data-stu-id="c1be5-177">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="c1be5-178">`[SkuSize <String>]`: Size-Bezeichner der Ressourcen-SKU.</span><span class="sxs-lookup"><span data-stu-id="c1be5-178">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="c1be5-179">`[SkuTier <String>]`: Dienstebene der Ressourcen-SKU.</span><span class="sxs-lookup"><span data-stu-id="c1be5-179">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="c1be5-180">`[SpotExpirationTime <DateTime?>]`: Der Zeitpunkt, zu dem die Serverfarm abläuft.</span><span class="sxs-lookup"><span data-stu-id="c1be5-180">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="c1be5-181">Nur gültig, wenn es sich um eine Spot Serverfarm handelt.</span><span class="sxs-lookup"><span data-stu-id="c1be5-181">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="c1be5-182">`[TargetWorkerCount <Int32?>]`: Skalieren der Worker-Anzahl</span><span class="sxs-lookup"><span data-stu-id="c1be5-182">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="c1be5-183">`[TargetWorkerSizeId <Int32?>]`: Skalierung der Worker-Größen-ID.</span><span class="sxs-lookup"><span data-stu-id="c1be5-183">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="c1be5-184">`[WorkerTierName <String>]`: Zielarbeitsebene, die dem App-Service Plan zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="c1be5-184">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="c1be5-185">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c1be5-185">RELATED LINKS</span></span>

