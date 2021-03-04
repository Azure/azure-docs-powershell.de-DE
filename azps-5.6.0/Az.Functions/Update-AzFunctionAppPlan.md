---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: 522de6721d92b76938843b28322b94b5cc6ce481
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924136"
---
# <span data-ttu-id="020ad-101">Update-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="020ad-101">Update-AzFunctionAppPlan</span></span>

## <span data-ttu-id="020ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="020ad-102">SYNOPSIS</span></span>
<span data-ttu-id="020ad-103">Aktualisiert einen Funktions-App-Dienstplan.</span><span class="sxs-lookup"><span data-stu-id="020ad-103">Updates a function app service plan.</span></span>

## <span data-ttu-id="020ad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="020ad-104">SYNTAX</span></span>

### <span data-ttu-id="020ad-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="020ad-105">ByName (Default)</span></span>
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="020ad-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="020ad-106">ByObjectInput</span></span>
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="020ad-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="020ad-107">DESCRIPTION</span></span>
<span data-ttu-id="020ad-108">Aktualisiert einen Funktions-App-Dienstplan.</span><span class="sxs-lookup"><span data-stu-id="020ad-108">Updates a function app service plan.</span></span>

## <span data-ttu-id="020ad-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="020ad-109">EXAMPLES</span></span>

### <span data-ttu-id="020ad-110">Beispiel 1: Aktualisieren eines App-Dienstplans auf EP2-Sku mit maximal zwanzig Mitarbeitern.</span><span class="sxs-lookup"><span data-stu-id="020ad-110">Example 1: Update an app service plan to EP2 sku with twenty maximum workers.</span></span>
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

<span data-ttu-id="020ad-111">Mit diesem Befehl wird ein App-Dienstplan mit 20 maximalen Mitarbeitern auf EP2-Sku aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="020ad-111">This command updates an app service plan to EP2 sku with twenty maximum workers.</span></span>

## <span data-ttu-id="020ad-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="020ad-112">PARAMETERS</span></span>

### <span data-ttu-id="020ad-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="020ad-113">-AsJob</span></span>
<span data-ttu-id="020ad-114">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="020ad-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="020ad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="020ad-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="020ad-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="020ad-116">-InputObject</span></span>
<span data-ttu-id="020ad-117">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="020ad-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="020ad-118">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="020ad-118">-MaximumWorkerCount</span></span>
<span data-ttu-id="020ad-119">Die maximale Anzahl von Mitarbeitern für den App-Dienstplan.</span><span class="sxs-lookup"><span data-stu-id="020ad-119">The maximum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="020ad-120">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="020ad-120">-MinimumWorkerCount</span></span>
<span data-ttu-id="020ad-121">Die Mindestanzahl von Mitarbeitern für den App-Dienstplan.</span><span class="sxs-lookup"><span data-stu-id="020ad-121">The minimum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="020ad-122">-Name</span><span class="sxs-lookup"><span data-stu-id="020ad-122">-Name</span></span>
<span data-ttu-id="020ad-123">Name des App Service-Plans.</span><span class="sxs-lookup"><span data-stu-id="020ad-123">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="020ad-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="020ad-124">-NoWait</span></span>
<span data-ttu-id="020ad-125">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="020ad-125">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="020ad-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="020ad-126">-ResourceGroupName</span></span>
<span data-ttu-id="020ad-127">Name der Ressourcengruppe, zu der die Ressource gehört.</span><span class="sxs-lookup"><span data-stu-id="020ad-127">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="020ad-128">-Sku</span><span class="sxs-lookup"><span data-stu-id="020ad-128">-Sku</span></span>
<span data-ttu-id="020ad-129">Die Sku des Plans.</span><span class="sxs-lookup"><span data-stu-id="020ad-129">The plan sku.</span></span>
<span data-ttu-id="020ad-130">Gültige Eingaben sind: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="020ad-130">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="020ad-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="020ad-131">-SubscriptionId</span></span>
<span data-ttu-id="020ad-132">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="020ad-132">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="020ad-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="020ad-133">-Tag</span></span>
<span data-ttu-id="020ad-134">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="020ad-134">Resource tags.</span></span>

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

### <span data-ttu-id="020ad-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="020ad-135">-Confirm</span></span>
<span data-ttu-id="020ad-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="020ad-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="020ad-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="020ad-137">-WhatIf</span></span>
<span data-ttu-id="020ad-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="020ad-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="020ad-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="020ad-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="020ad-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="020ad-140">CommonParameters</span></span>
<span data-ttu-id="020ad-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="020ad-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="020ad-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="020ad-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="020ad-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="020ad-143">INPUTS</span></span>

### <span data-ttu-id="020ad-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="020ad-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="020ad-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="020ad-145">OUTPUTS</span></span>

### <span data-ttu-id="020ad-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="020ad-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="020ad-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="020ad-147">NOTES</span></span>

<span data-ttu-id="020ad-148">ALIASE</span><span class="sxs-lookup"><span data-stu-id="020ad-148">ALIASES</span></span>

<span data-ttu-id="020ad-149">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="020ad-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="020ad-150">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="020ad-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="020ad-151">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="020ad-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="020ad-152">INPUTOBJECT <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="020ad-152">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="020ad-153">`Location <String>`: Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="020ad-153">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="020ad-154">`[Kind <String>]`: Art der Ressource.</span><span class="sxs-lookup"><span data-stu-id="020ad-154">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="020ad-155">`[Tag <IResourceTags>]`: Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="020ad-155">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="020ad-156">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="020ad-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="020ad-157">`[Capacity <Int32?>]`: Aktuelle Anzahl der der Ressource zugewiesenen Instanzen.</span><span class="sxs-lookup"><span data-stu-id="020ad-157">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="020ad-158">`[FreeOfferExpirationTime <DateTime?>]`: Der Zeitpunkt, zu dem das kostenlose Angebot für die Serverfarm abläuft.</span><span class="sxs-lookup"><span data-stu-id="020ad-158">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="020ad-159">`[HostingEnvironmentProfileId <String>]`: Ressourcen-ID der App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="020ad-159">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="020ad-160">`[HyperV <Boolean?>]`: Wenn Hyper-V-Container-App-Dienstplan <code>true</code> , <code>false</code> andernfalls.</span><span class="sxs-lookup"><span data-stu-id="020ad-160">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="020ad-161">`[IsSpot <Boolean?>]`: Wenn <code>true</code> , besitzt dieser App Service Plan Spotinstanzen.</span><span class="sxs-lookup"><span data-stu-id="020ad-161">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="020ad-162">`[IsXenon <Boolean?>]`: Veraltet: Wenn Hyper-V-Container-App-Dienstplan <code>true</code> , <code>false</code> andernfalls.</span><span class="sxs-lookup"><span data-stu-id="020ad-162">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="020ad-163">`[MaximumElasticWorkerCount <Int32?>]`: Maximale Anzahl der für diesen Serviceplan für die FlexibleScaleEnabled-App zulässigen Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="020ad-163">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="020ad-164">`[PerSiteScaling <Boolean?>]`: Wenn diesem App Service-Plan zugewiesene Apps <code>true</code> unabhängig skaliert werden können.</span><span class="sxs-lookup"><span data-stu-id="020ad-164">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="020ad-165">Wenn <code>false</code> apps assigned to this App Service plan will scale to all instances of the plan.</span><span class="sxs-lookup"><span data-stu-id="020ad-165">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="020ad-166">`[Reserved <Boolean?>]`: Wenn linux app service plan <code>true</code> , <code>false</code> andernfalls.</span><span class="sxs-lookup"><span data-stu-id="020ad-166">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="020ad-167">`[SkuCapability <ICapability[]>]`: Funktionen der SKU, z. B. ist Traffic Manager aktiviert?</span><span class="sxs-lookup"><span data-stu-id="020ad-167">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="020ad-168">`[Name <String>]`: Name der SKU-Funktion.</span><span class="sxs-lookup"><span data-stu-id="020ad-168">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="020ad-169">`[Reason <String>]`: Grund für die SKU-Funktion.</span><span class="sxs-lookup"><span data-stu-id="020ad-169">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="020ad-170">`[Value <String>]`: Wert der SKU-Funktion.</span><span class="sxs-lookup"><span data-stu-id="020ad-170">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="020ad-171">`[SkuCapacityDefault <Int32?>]`: Standardanzahl der Mitarbeiter für diese App Service Plan SKU.</span><span class="sxs-lookup"><span data-stu-id="020ad-171">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="020ad-172">`[SkuCapacityMaximum <Int32?>]`: Maximale Anzahl von Mitarbeitern für diese App Service Plan SKU.</span><span class="sxs-lookup"><span data-stu-id="020ad-172">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="020ad-173">`[SkuCapacityMinimum <Int32?>]`: Mindestanzahl von Mitarbeitern für diese App Service Plan SKU.</span><span class="sxs-lookup"><span data-stu-id="020ad-173">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="020ad-174">`[SkuCapacityScaleType <String>]`: Verfügbare Skalierungskonfigurationen für einen App Service-Plan.</span><span class="sxs-lookup"><span data-stu-id="020ad-174">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="020ad-175">`[SkuFamily <String>]`: Familiencode der Ressourcen-SKU.</span><span class="sxs-lookup"><span data-stu-id="020ad-175">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="020ad-176">`[SkuLocation <String[]>]`: Speicherorte der SKU.</span><span class="sxs-lookup"><span data-stu-id="020ad-176">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="020ad-177">`[SkuName <String>]`: Name der Ressourcen-SKU.</span><span class="sxs-lookup"><span data-stu-id="020ad-177">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="020ad-178">`[SkuSize <String>]`: Größenbezeichner der Ressourcen-SKU.</span><span class="sxs-lookup"><span data-stu-id="020ad-178">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="020ad-179">`[SkuTier <String>]`: Dienstebene der Ressourcen-SKU.</span><span class="sxs-lookup"><span data-stu-id="020ad-179">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="020ad-180">`[SpotExpirationTime <DateTime?>]`: Der Zeitpunkt, zu dem die Serverfarm abläuft.</span><span class="sxs-lookup"><span data-stu-id="020ad-180">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="020ad-181">Gültig nur, wenn es sich um eine Spotserverfarm handelt.</span><span class="sxs-lookup"><span data-stu-id="020ad-181">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="020ad-182">`[TargetWorkerCount <Int32?>]`: Skalierung der Workeranzahl.</span><span class="sxs-lookup"><span data-stu-id="020ad-182">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="020ad-183">`[TargetWorkerSizeId <Int32?>]`: Skalierung der Mitarbeitergröße ID.</span><span class="sxs-lookup"><span data-stu-id="020ad-183">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="020ad-184">`[WorkerTierName <String>]`: Zielarbeiterebene, die dem App Service-Plan zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="020ad-184">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="020ad-185">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="020ad-185">RELATED LINKS</span></span>

