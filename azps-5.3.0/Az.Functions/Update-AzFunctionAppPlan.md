---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469723"
---
# <span data-ttu-id="17cff-101">Update-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="17cff-101">Update-AzFunctionAppPlan</span></span>

## <span data-ttu-id="17cff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17cff-102">SYNOPSIS</span></span>
<span data-ttu-id="17cff-103">Aktualisiert einen Funktions-App-Serviceplan.</span><span class="sxs-lookup"><span data-stu-id="17cff-103">Updates a function app service plan.</span></span>

## <span data-ttu-id="17cff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17cff-104">SYNTAX</span></span>

### <span data-ttu-id="17cff-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="17cff-105">ByName (Default)</span></span>
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="17cff-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="17cff-106">ByObjectInput</span></span>
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="17cff-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17cff-107">DESCRIPTION</span></span>
<span data-ttu-id="17cff-108">Aktualisiert einen Funktions-App-Serviceplan.</span><span class="sxs-lookup"><span data-stu-id="17cff-108">Updates a function app service plan.</span></span>

## <span data-ttu-id="17cff-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="17cff-109">EXAMPLES</span></span>

### <span data-ttu-id="17cff-110">Beispiel 1: Aktualisieren eines App-Serviceplans auf eine EP2-SKU mit maximal 20 Mitarbeitern.</span><span class="sxs-lookup"><span data-stu-id="17cff-110">Example 1: Update an app service plan to EP2 sku with twenty maximum workers.</span></span>
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

<span data-ttu-id="17cff-111">Mit diesem Befehl wird ein App-Service-Plan auf eine EP2-SKU mit maximal 20 Mitarbeitern aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="17cff-111">This command updates an app service plan to EP2 sku with twenty maximum workers.</span></span>

## <span data-ttu-id="17cff-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17cff-112">PARAMETERS</span></span>

### <span data-ttu-id="17cff-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17cff-113">-AsJob</span></span>
<span data-ttu-id="17cff-114">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="17cff-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="17cff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17cff-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="17cff-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17cff-116">-InputObject</span></span>
<span data-ttu-id="17cff-117">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="17cff-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="17cff-118">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="17cff-118">-MaximumWorkerCount</span></span>
<span data-ttu-id="17cff-119">Die maximale Anzahl von Mitarbeitern für den App-Serviceplan.</span><span class="sxs-lookup"><span data-stu-id="17cff-119">The maximum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="17cff-120">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="17cff-120">-MinimumWorkerCount</span></span>
<span data-ttu-id="17cff-121">Die Mindestanzahl von Mitarbeitern für den App-Serviceplan.</span><span class="sxs-lookup"><span data-stu-id="17cff-121">The minimum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="17cff-122">-Name</span><span class="sxs-lookup"><span data-stu-id="17cff-122">-Name</span></span>
<span data-ttu-id="17cff-123">Name des App-Service-Plans.</span><span class="sxs-lookup"><span data-stu-id="17cff-123">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="17cff-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="17cff-124">-NoWait</span></span>
<span data-ttu-id="17cff-125">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="17cff-125">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="17cff-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17cff-126">-ResourceGroupName</span></span>
<span data-ttu-id="17cff-127">Der Name der Ressourcengruppe, zu der die Ressource gehört.</span><span class="sxs-lookup"><span data-stu-id="17cff-127">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="17cff-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="17cff-128">-Sku</span></span>
<span data-ttu-id="17cff-129">Die SKU des Plans.</span><span class="sxs-lookup"><span data-stu-id="17cff-129">The plan sku.</span></span>
<span data-ttu-id="17cff-130">Gültige Eingaben sind: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="17cff-130">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="17cff-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="17cff-131">-SubscriptionId</span></span>
<span data-ttu-id="17cff-132">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="17cff-132">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="17cff-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="17cff-133">-Tag</span></span>
<span data-ttu-id="17cff-134">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="17cff-134">Resource tags.</span></span>

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

### <span data-ttu-id="17cff-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17cff-135">-Confirm</span></span>
<span data-ttu-id="17cff-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="17cff-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17cff-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="17cff-137">-WhatIf</span></span>
<span data-ttu-id="17cff-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="17cff-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17cff-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="17cff-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17cff-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17cff-140">CommonParameters</span></span>
<span data-ttu-id="17cff-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17cff-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17cff-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17cff-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17cff-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="17cff-143">INPUTS</span></span>

### <span data-ttu-id="17cff-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="17cff-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="17cff-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="17cff-145">OUTPUTS</span></span>

### <span data-ttu-id="17cff-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="17cff-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="17cff-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="17cff-147">NOTES</span></span>

<span data-ttu-id="17cff-148">ALIASE</span><span class="sxs-lookup"><span data-stu-id="17cff-148">ALIASES</span></span>

<span data-ttu-id="17cff-149">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="17cff-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="17cff-150">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="17cff-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="17cff-151">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="17cff-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="17cff-152">INPUTOBJECT <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="17cff-152">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="17cff-153">`Location <String>`: Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="17cff-153">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="17cff-154">`[Kind <String>]`: Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="17cff-154">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="17cff-155">`[Tag <IResourceTags>]`: Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="17cff-155">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="17cff-156">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="17cff-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="17cff-157">`[Capacity <Int32?>]`: Die aktuelle Anzahl von Instanzen, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="17cff-157">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="17cff-158">`[FreeOfferExpirationTime <DateTime?>]`: Der Zeitpunkt, zu dem das kostenlose Angebot für die Serverfarm abläuft.</span><span class="sxs-lookup"><span data-stu-id="17cff-158">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="17cff-159">`[HostingEnvironmentProfileId <String>]`: Ressourcen-ID der App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="17cff-159">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="17cff-160">`[HyperV <Boolean?>]`: Wenn andernfalls der Hyper-V-Container-App-Dienstplan <code>true</code> <code>false</code> verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="17cff-160">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="17cff-161">`[IsSpot <Boolean?>]`: <code>true</code> Falls, besitzt dieser App-Serviceplan Spotinstanzen.</span><span class="sxs-lookup"><span data-stu-id="17cff-161">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="17cff-162">`[IsXenon <Boolean?>]`: Veraltet: Wenn andernfalls der Hyper-V-Container-App-Dienstplan <code>true</code> <code>false</code> verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="17cff-162">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="17cff-163">`[MaximumElasticWorkerCount <Int32?>]`: Maximal zulässige Anzahl von Arbeitskräften für diesen Serviceplan der App "Skalaenabled".</span><span class="sxs-lookup"><span data-stu-id="17cff-163">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="17cff-164">`[PerSiteScaling <Boolean?>]`: <code>true</code> Falls, können Apps, die diesem App Service Plan zugewiesen sind, unabhängig skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="17cff-164">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="17cff-165">Wenn <code>false</code> diesem App -Service-Plan zugewiesene Apps auf alle Instanzen des Plans skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="17cff-165">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="17cff-166">`[Reserved <Boolean?>]`: Wenn Linux-App-Serviceplan <code>true</code> , <code>false</code> andernfalls.</span><span class="sxs-lookup"><span data-stu-id="17cff-166">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="17cff-167">`[SkuCapability <ICapability[]>]`: Funktionen der SKU, z. B. aktivierter Datenverkehrs-Manager?</span><span class="sxs-lookup"><span data-stu-id="17cff-167">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="17cff-168">`[Name <String>]`: Name der SKU-Funktion.</span><span class="sxs-lookup"><span data-stu-id="17cff-168">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="17cff-169">`[Reason <String>]`: Grund der SKU-Funktion.</span><span class="sxs-lookup"><span data-stu-id="17cff-169">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="17cff-170">`[Value <String>]`: Wert der SKU-Funktion.</span><span class="sxs-lookup"><span data-stu-id="17cff-170">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="17cff-171">`[SkuCapacityDefault <Int32?>]`: Standardanzahl von Mitarbeitern für diese App Service Plan-SKU.</span><span class="sxs-lookup"><span data-stu-id="17cff-171">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="17cff-172">`[SkuCapacityMaximum <Int32?>]`: Maximale Anzahl von Mitarbeitern für diese App Service Plan-SKU.</span><span class="sxs-lookup"><span data-stu-id="17cff-172">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="17cff-173">`[SkuCapacityMinimum <Int32?>]`: Mindestanzahl von Mitarbeitern für diese App Service Plan-SKU.</span><span class="sxs-lookup"><span data-stu-id="17cff-173">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="17cff-174">`[SkuCapacityScaleType <String>]`: Verfügbare Skalierungskonfigurationen für einen App-Service-Plan.</span><span class="sxs-lookup"><span data-stu-id="17cff-174">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="17cff-175">`[SkuFamily <String>]`: Familiencode der Ressourcen-SKU.</span><span class="sxs-lookup"><span data-stu-id="17cff-175">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="17cff-176">`[SkuLocation <String[]>]`: Speicherorte der SKU.</span><span class="sxs-lookup"><span data-stu-id="17cff-176">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="17cff-177">`[SkuName <String>]`: Name der Ressourcen-SKU.</span><span class="sxs-lookup"><span data-stu-id="17cff-177">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="17cff-178">`[SkuSize <String>]`: Größenbezeichner der Ressourcen-SKU.</span><span class="sxs-lookup"><span data-stu-id="17cff-178">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="17cff-179">`[SkuTier <String>]`: Dienstebene der Ressourcen-SKU.</span><span class="sxs-lookup"><span data-stu-id="17cff-179">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="17cff-180">`[SpotExpirationTime <DateTime?>]`: Der Zeitpunkt, zu dem die Serverfarm abläuft.</span><span class="sxs-lookup"><span data-stu-id="17cff-180">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="17cff-181">Nur gültig, wenn es sich um eine Spotserverfarm handelt.</span><span class="sxs-lookup"><span data-stu-id="17cff-181">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="17cff-182">`[TargetWorkerCount <Int32?>]`: Anzahl der Skalierungsmitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="17cff-182">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="17cff-183">`[TargetWorkerSizeId <Int32?>]`: Skalierungs-Worker-Größen-ID.</span><span class="sxs-lookup"><span data-stu-id="17cff-183">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="17cff-184">`[WorkerTierName <String>]`: Dem App -Dienstplan zugewiesene Zielworkerebene.</span><span class="sxs-lookup"><span data-stu-id="17cff-184">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="17cff-185">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="17cff-185">RELATED LINKS</span></span>

