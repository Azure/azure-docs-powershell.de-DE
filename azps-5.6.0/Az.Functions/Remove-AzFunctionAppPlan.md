---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: e930a0848f39ec94cb6eeb4ef290b1842ea6793a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940435"
---
# <span data-ttu-id="05890-101">Remove-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="05890-101">Remove-AzFunctionAppPlan</span></span>

## <span data-ttu-id="05890-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05890-102">SYNOPSIS</span></span>
<span data-ttu-id="05890-103">Löscht einen Funktions-App-Plan.</span><span class="sxs-lookup"><span data-stu-id="05890-103">Deletes a function app plan.</span></span>

## <span data-ttu-id="05890-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05890-104">SYNTAX</span></span>

### <span data-ttu-id="05890-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="05890-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="05890-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="05890-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="05890-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="05890-107">DESCRIPTION</span></span>
<span data-ttu-id="05890-108">Löscht einen Funktions-App-Plan.</span><span class="sxs-lookup"><span data-stu-id="05890-108">Deletes a function app plan.</span></span>

## <span data-ttu-id="05890-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="05890-109">EXAMPLES</span></span>

### <span data-ttu-id="05890-110">Beispiel 1: Holen Sie sich einen Funktions-App-Plan nach Name, und löschen Sie ihn.</span><span class="sxs-lookup"><span data-stu-id="05890-110">Example 1: Get a function app plan by name and delete it.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

<span data-ttu-id="05890-111">Dieser Befehl ruft einen Funktions-App-Plan nach Name ab und löscht ihn.</span><span class="sxs-lookup"><span data-stu-id="05890-111">This command gets a function app plan by name and deletes it.</span></span>

### <span data-ttu-id="05890-112">Beispiel 2: Löschen eines Funktions-App-Plans nach Name.</span><span class="sxs-lookup"><span data-stu-id="05890-112">Example 2: Delete a function app plan by name.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="05890-113">Mit diesem Befehl wird ein Funktions-App-Plan nach Name gelöscht.</span><span class="sxs-lookup"><span data-stu-id="05890-113">This command deletes a function app plan by name.</span></span>

## <span data-ttu-id="05890-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="05890-114">PARAMETERS</span></span>

### <span data-ttu-id="05890-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05890-115">-DefaultProfile</span></span>
<span data-ttu-id="05890-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="05890-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05890-117">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="05890-117">-Force</span></span>
<span data-ttu-id="05890-118">Erzwingt das Cmdlet, den Funktions-App-Plan zu entfernen, ohne zur Bestätigung aufgefordert zu werden.</span><span class="sxs-lookup"><span data-stu-id="05890-118">Forces the cmdlet to remove the function app plan without prompting for confirmation.</span></span>

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

### <span data-ttu-id="05890-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05890-119">-InputObject</span></span>
<span data-ttu-id="05890-120">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="05890-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="05890-121">-Name</span><span class="sxs-lookup"><span data-stu-id="05890-121">-Name</span></span>
<span data-ttu-id="05890-122">Der Name der Funktions-App.</span><span class="sxs-lookup"><span data-stu-id="05890-122">The name of function app.</span></span>

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

### <span data-ttu-id="05890-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05890-123">-PassThru</span></span>
<span data-ttu-id="05890-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="05890-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="05890-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05890-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="05890-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05890-126">-SubscriptionId</span></span>
<span data-ttu-id="05890-127">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="05890-127">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="05890-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="05890-128">-Confirm</span></span>
<span data-ttu-id="05890-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="05890-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05890-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05890-130">-WhatIf</span></span>
<span data-ttu-id="05890-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="05890-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05890-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="05890-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05890-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05890-133">CommonParameters</span></span>
<span data-ttu-id="05890-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05890-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05890-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05890-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05890-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="05890-136">INPUTS</span></span>

### <span data-ttu-id="05890-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="05890-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="05890-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="05890-138">OUTPUTS</span></span>

### <span data-ttu-id="05890-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="05890-139">System.Boolean</span></span>

## <span data-ttu-id="05890-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="05890-140">NOTES</span></span>

<span data-ttu-id="05890-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="05890-141">ALIASES</span></span>

<span data-ttu-id="05890-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="05890-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="05890-143">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="05890-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="05890-144">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="05890-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="05890-145">INPUTOBJECT <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="05890-145">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="05890-146">`Location <String>`: Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="05890-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="05890-147">`[Kind <String>]`: Art der Ressource.</span><span class="sxs-lookup"><span data-stu-id="05890-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="05890-148">`[Tag <IResourceTags>]`: Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="05890-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="05890-149">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="05890-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="05890-150">`[Capacity <Int32?>]`: Aktuelle Anzahl der der Ressource zugewiesenen Instanzen.</span><span class="sxs-lookup"><span data-stu-id="05890-150">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="05890-151">`[FreeOfferExpirationTime <DateTime?>]`: Der Zeitpunkt, zu dem das kostenlose Angebot für die Serverfarm abläuft.</span><span class="sxs-lookup"><span data-stu-id="05890-151">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="05890-152">`[HostingEnvironmentProfileId <String>]`: Ressourcen-ID der App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="05890-152">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="05890-153">`[HyperV <Boolean?>]`: Wenn Hyper-V-Container-App-Dienstplan <code>true</code> , <code>false</code> andernfalls.</span><span class="sxs-lookup"><span data-stu-id="05890-153">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="05890-154">`[IsSpot <Boolean?>]`: Wenn <code>true</code> , besitzt dieser App Service Plan Spotinstanzen.</span><span class="sxs-lookup"><span data-stu-id="05890-154">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="05890-155">`[IsXenon <Boolean?>]`: Veraltet: Wenn Hyper-V-Container-App-Dienstplan <code>true</code> , <code>false</code> andernfalls.</span><span class="sxs-lookup"><span data-stu-id="05890-155">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="05890-156">`[MaximumElasticWorkerCount <Int32?>]`: Maximale Anzahl der für diesen Serviceplan für die FlexibleScaleEnabled-App zulässigen Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="05890-156">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="05890-157">`[PerSiteScaling <Boolean?>]`: Wenn diesem App Service-Plan zugewiesene Apps <code>true</code> unabhängig skaliert werden können.</span><span class="sxs-lookup"><span data-stu-id="05890-157">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="05890-158">Wenn <code>false</code> apps assigned to this App Service plan will scale to all instances of the plan.</span><span class="sxs-lookup"><span data-stu-id="05890-158">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="05890-159">`[Reserved <Boolean?>]`: Wenn linux app service plan <code>true</code> , <code>false</code> andernfalls.</span><span class="sxs-lookup"><span data-stu-id="05890-159">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="05890-160">`[SkuCapability <ICapability[]>]`: Funktionen der SKU, z. B. ist Traffic Manager aktiviert?</span><span class="sxs-lookup"><span data-stu-id="05890-160">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="05890-161">`[Name <String>]`: Name der SKU-Funktion.</span><span class="sxs-lookup"><span data-stu-id="05890-161">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="05890-162">`[Reason <String>]`: Grund für die SKU-Funktion.</span><span class="sxs-lookup"><span data-stu-id="05890-162">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="05890-163">`[Value <String>]`: Wert der SKU-Funktion.</span><span class="sxs-lookup"><span data-stu-id="05890-163">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="05890-164">`[SkuCapacityDefault <Int32?>]`: Standardanzahl der Mitarbeiter für diese App Service Plan SKU.</span><span class="sxs-lookup"><span data-stu-id="05890-164">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="05890-165">`[SkuCapacityMaximum <Int32?>]`: Maximale Anzahl von Mitarbeitern für diese App Service Plan SKU.</span><span class="sxs-lookup"><span data-stu-id="05890-165">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="05890-166">`[SkuCapacityMinimum <Int32?>]`: Mindestanzahl von Mitarbeitern für diese App Service Plan SKU.</span><span class="sxs-lookup"><span data-stu-id="05890-166">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="05890-167">`[SkuCapacityScaleType <String>]`: Verfügbare Skalierungskonfigurationen für einen App Service-Plan.</span><span class="sxs-lookup"><span data-stu-id="05890-167">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="05890-168">`[SkuFamily <String>]`: Familiencode der Ressourcen-SKU.</span><span class="sxs-lookup"><span data-stu-id="05890-168">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="05890-169">`[SkuLocation <String[]>]`: Speicherorte der SKU.</span><span class="sxs-lookup"><span data-stu-id="05890-169">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="05890-170">`[SkuName <String>]`: Name der Ressourcen-SKU.</span><span class="sxs-lookup"><span data-stu-id="05890-170">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="05890-171">`[SkuSize <String>]`: Größenbezeichner der Ressourcen-SKU.</span><span class="sxs-lookup"><span data-stu-id="05890-171">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="05890-172">`[SkuTier <String>]`: Dienstebene der Ressourcen-SKU.</span><span class="sxs-lookup"><span data-stu-id="05890-172">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="05890-173">`[SpotExpirationTime <DateTime?>]`: Der Zeitpunkt, zu dem die Serverfarm abläuft.</span><span class="sxs-lookup"><span data-stu-id="05890-173">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="05890-174">Gültig nur, wenn es sich um eine Spotserverfarm handelt.</span><span class="sxs-lookup"><span data-stu-id="05890-174">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="05890-175">`[TargetWorkerCount <Int32?>]`: Skalierung der Workeranzahl.</span><span class="sxs-lookup"><span data-stu-id="05890-175">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="05890-176">`[TargetWorkerSizeId <Int32?>]`: Skalierung der Mitarbeitergröße ID.</span><span class="sxs-lookup"><span data-stu-id="05890-176">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="05890-177">`[WorkerTierName <String>]`: Zielarbeiterebene, die dem App Service-Plan zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="05890-177">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="05890-178">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="05890-178">RELATED LINKS</span></span>

