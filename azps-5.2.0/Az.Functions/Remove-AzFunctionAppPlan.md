---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291340"
---
# <span data-ttu-id="e4eb0-101">Remove-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="e4eb0-101">Remove-AzFunctionAppPlan</span></span>

## <span data-ttu-id="e4eb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4eb0-102">SYNOPSIS</span></span>
<span data-ttu-id="e4eb0-103">Löscht einen Funktions-App-Plan.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-103">Deletes a function app plan.</span></span>

## <span data-ttu-id="e4eb0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4eb0-104">SYNTAX</span></span>

### <span data-ttu-id="e4eb0-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e4eb0-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e4eb0-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="e4eb0-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e4eb0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4eb0-107">DESCRIPTION</span></span>
<span data-ttu-id="e4eb0-108">Löscht einen Funktions-App-Plan.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-108">Deletes a function app plan.</span></span>

## <span data-ttu-id="e4eb0-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e4eb0-109">EXAMPLES</span></span>

### <span data-ttu-id="e4eb0-110">Beispiel 1: Einen Funktions-App-Plan nach Name erhalten und löschen.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-110">Example 1: Get a function app plan by name and delete it.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

<span data-ttu-id="e4eb0-111">Dieser Befehl ruft einen Funktions-App-Plan nach Name ab und löscht ihn.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-111">This command gets a function app plan by name and deletes it.</span></span>

### <span data-ttu-id="e4eb0-112">Beispiel 2: Löschen eines Funktions-App-Plans nach Name.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-112">Example 2: Delete a function app plan by name.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="e4eb0-113">Mit diesem Befehl wird ein Funktions-App-Plan nach Name gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-113">This command deletes a function app plan by name.</span></span>

## <span data-ttu-id="e4eb0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4eb0-114">PARAMETERS</span></span>

### <span data-ttu-id="e4eb0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4eb0-115">-DefaultProfile</span></span>
<span data-ttu-id="e4eb0-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4eb0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e4eb0-117">-Force</span></span>
<span data-ttu-id="e4eb0-118">Erzwingt das Cmdlet, den Funktions-App-Plan ohne Bestätigungsaufforderung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-118">Forces the cmdlet to remove the function app plan without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e4eb0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4eb0-119">-InputObject</span></span>
<span data-ttu-id="e4eb0-120">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e4eb0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e4eb0-121">-Name</span></span>
<span data-ttu-id="e4eb0-122">Der Name der Funktions-App.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-122">The name of function app.</span></span>

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

### <span data-ttu-id="e4eb0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4eb0-123">-PassThru</span></span>
<span data-ttu-id="e4eb0-124">Gibt "true" zurück, wenn der Befehl erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="e4eb0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4eb0-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="e4eb0-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e4eb0-126">-SubscriptionId</span></span>
<span data-ttu-id="e4eb0-127">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-127">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="e4eb0-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4eb0-128">-Confirm</span></span>
<span data-ttu-id="e4eb0-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4eb0-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e4eb0-130">-WhatIf</span></span>
<span data-ttu-id="e4eb0-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4eb0-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4eb0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4eb0-133">CommonParameters</span></span>
<span data-ttu-id="e4eb0-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4eb0-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4eb0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4eb0-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e4eb0-136">INPUTS</span></span>

### <span data-ttu-id="e4eb0-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e4eb0-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="e4eb0-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e4eb0-138">OUTPUTS</span></span>

### <span data-ttu-id="e4eb0-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e4eb0-139">System.Boolean</span></span>

## <span data-ttu-id="e4eb0-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e4eb0-140">NOTES</span></span>

<span data-ttu-id="e4eb0-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e4eb0-141">ALIASES</span></span>

<span data-ttu-id="e4eb0-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="e4eb0-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e4eb0-143">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e4eb0-144">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e4eb0-145">INPUTOBJECT <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="e4eb0-145">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="e4eb0-146">`Location <String>`: Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="e4eb0-147">`[Kind <String>]`: Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="e4eb0-148">`[Tag <IResourceTags>]`: Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="e4eb0-149">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="e4eb0-150">`[Capacity <Int32?>]`: Aktuelle Anzahl von Instanzen, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-150">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="e4eb0-151">`[FreeOfferExpirationTime <DateTime?>]`: Der Zeitpunkt, zu dem das kostenlose Angebot für die Serverfarm abläuft.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-151">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="e4eb0-152">`[HostingEnvironmentProfileId <String>]`: Ressourcen-ID der App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-152">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="e4eb0-153">`[HyperV <Boolean?>]`: Wenn andernfalls der Hyper-V-Container-App-Dienstplan <code>true</code> <code>false</code> verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-153">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="e4eb0-154">`[IsSpot <Boolean?>]`: Ist <code>true</code> dies der Fall, besitzt dieser App-Serviceplan Spotinstanzen.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-154">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="e4eb0-155">`[IsXenon <Boolean?>]`: Veraltet: Wenn andernfalls der Hyper-V-Container-App-Dienstplan <code>true</code> <code>false</code> verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-155">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="e4eb0-156">`[MaximumElasticWorkerCount <Int32?>]`: Maximal zulässige Anzahl von Arbeitskräften für diesen Serviceplan der App "Skalaenabled".</span><span class="sxs-lookup"><span data-stu-id="e4eb0-156">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="e4eb0-157">`[PerSiteScaling <Boolean?>]`: Wenn <code>true</code> apps, die diesem App Service Plan zugewiesen sind, unabhängig skaliert werden können.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-157">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="e4eb0-158">Wenn <code>false</code> diesem App -Service-Plan zugewiesene Apps auf alle Instanzen des Plans skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-158">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="e4eb0-159">`[Reserved <Boolean?>]`: Wenn Linux-App-Serviceplan <code>true</code> , <code>false</code> andernfalls.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-159">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="e4eb0-160">`[SkuCapability <ICapability[]>]`: Funktionen der SKU, z. B. aktivierter Datenverkehrs-Manager?</span><span class="sxs-lookup"><span data-stu-id="e4eb0-160">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="e4eb0-161">`[Name <String>]`: Name der SKU-Funktion.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-161">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="e4eb0-162">`[Reason <String>]`: Grund der SKU-Funktion.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-162">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="e4eb0-163">`[Value <String>]`: Wert der SKU-Funktion.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-163">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="e4eb0-164">`[SkuCapacityDefault <Int32?>]`: Standardanzahl von Mitarbeitern für diese App Service Plan-SKU.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-164">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="e4eb0-165">`[SkuCapacityMaximum <Int32?>]`: Maximale Anzahl von Mitarbeitern für diese App Service Plan-SKU.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-165">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="e4eb0-166">`[SkuCapacityMinimum <Int32?>]`: Mindestanzahl von Mitarbeitern für diese App Service Plan-SKU.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-166">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="e4eb0-167">`[SkuCapacityScaleType <String>]`: Verfügbare Skalierungskonfigurationen für einen App-Service-Plan.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-167">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="e4eb0-168">`[SkuFamily <String>]`: Familiencode der Ressourcen-SKU.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-168">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="e4eb0-169">`[SkuLocation <String[]>]`: Speicherorte der SKU.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-169">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="e4eb0-170">`[SkuName <String>]`: Name der Ressourcen-SKU.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-170">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="e4eb0-171">`[SkuSize <String>]`: Größenbezeichner der Ressourcen-SKU.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-171">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="e4eb0-172">`[SkuTier <String>]`: Dienstebene der Ressourcen-SKU.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-172">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="e4eb0-173">`[SpotExpirationTime <DateTime?>]`: Der Zeitpunkt, zu dem die Serverfarm abläuft.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-173">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="e4eb0-174">Nur gültig, wenn es sich um eine Spotserverfarm handelt.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-174">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="e4eb0-175">`[TargetWorkerCount <Int32?>]`: Anzahl der Skalierungsmitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-175">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="e4eb0-176">`[TargetWorkerSizeId <Int32?>]`: Skalierungs-Worker-Größen-ID.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-176">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="e4eb0-177">`[WorkerTierName <String>]`: Dem App -Dienstplan zugewiesene Zielworkerebene.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-177">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="e4eb0-178">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e4eb0-178">RELATED LINKS</span></span>

