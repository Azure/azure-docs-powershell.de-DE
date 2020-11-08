---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175623"
---
# <span data-ttu-id="a6df3-101">Remove-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="a6df3-101">Remove-AzFunctionAppPlan</span></span>

## <span data-ttu-id="a6df3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a6df3-102">SYNOPSIS</span></span>
<span data-ttu-id="a6df3-103">Löscht einen Funktions-APP-Plan.</span><span class="sxs-lookup"><span data-stu-id="a6df3-103">Deletes a function app plan.</span></span>

## <span data-ttu-id="a6df3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6df3-104">SYNTAX</span></span>

### <span data-ttu-id="a6df3-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a6df3-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a6df3-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="a6df3-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a6df3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a6df3-107">DESCRIPTION</span></span>
<span data-ttu-id="a6df3-108">Löscht einen Funktions-APP-Plan.</span><span class="sxs-lookup"><span data-stu-id="a6df3-108">Deletes a function app plan.</span></span>

## <span data-ttu-id="a6df3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a6df3-109">EXAMPLES</span></span>

### <span data-ttu-id="a6df3-110">Beispiel 1: Rufen Sie einen Funktions-APP-Plan nach Namen ab, und löschen Sie ihn.</span><span class="sxs-lookup"><span data-stu-id="a6df3-110">Example 1: Get a function app plan by name and delete it.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

<span data-ttu-id="a6df3-111">Dieser Befehl ruft einen Funktions-APP-Plan nach Name ab und löscht ihn.</span><span class="sxs-lookup"><span data-stu-id="a6df3-111">This command gets a function app plan by name and deletes it.</span></span>

### <span data-ttu-id="a6df3-112">Beispiel 2: Löschen eines Funktions-APP-Plans nach Name</span><span class="sxs-lookup"><span data-stu-id="a6df3-112">Example 2: Delete a function app plan by name.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="a6df3-113">Dieser Befehl löscht einen Funktions-APP-Plan nach Namen.</span><span class="sxs-lookup"><span data-stu-id="a6df3-113">This command deletes a function app plan by name.</span></span>

## <span data-ttu-id="a6df3-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6df3-114">PARAMETERS</span></span>

### <span data-ttu-id="a6df3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6df3-115">-DefaultProfile</span></span>
<span data-ttu-id="a6df3-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a6df3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6df3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a6df3-117">-Force</span></span>
<span data-ttu-id="a6df3-118">Erzwingt, dass das Cmdlet den Funktions-APP-Plan entfernt, ohne die Bestätigung zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="a6df3-118">Forces the cmdlet to remove the function app plan without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a6df3-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a6df3-119">-InputObject</span></span>
<span data-ttu-id="a6df3-120">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a6df3-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a6df3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a6df3-121">-Name</span></span>
<span data-ttu-id="a6df3-122">Der Name der Funktions-APP.</span><span class="sxs-lookup"><span data-stu-id="a6df3-122">The name of function app.</span></span>

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

### <span data-ttu-id="a6df3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6df3-123">-PassThru</span></span>
<span data-ttu-id="a6df3-124">Gibt "true" zurück, wenn der Befehl erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="a6df3-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="a6df3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6df3-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="a6df3-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="a6df3-126">-SubscriptionId</span></span>
<span data-ttu-id="a6df3-127">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="a6df3-127">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="a6df3-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a6df3-128">-Confirm</span></span>
<span data-ttu-id="a6df3-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a6df3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6df3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6df3-130">-WhatIf</span></span>
<span data-ttu-id="a6df3-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6df3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6df3-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6df3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6df3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6df3-133">CommonParameters</span></span>
<span data-ttu-id="a6df3-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6df3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6df3-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6df3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6df3-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a6df3-136">INPUTS</span></span>

### <span data-ttu-id="a6df3-137">Microsoft. Azure. PowerShell. Cmdlets. Functions. Models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a6df3-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="a6df3-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a6df3-138">OUTPUTS</span></span>

### <span data-ttu-id="a6df3-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a6df3-139">System.Boolean</span></span>

## <span data-ttu-id="a6df3-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="a6df3-140">NOTES</span></span>

<span data-ttu-id="a6df3-141">Aliase</span><span class="sxs-lookup"><span data-stu-id="a6df3-141">ALIASES</span></span>

<span data-ttu-id="a6df3-142">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a6df3-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a6df3-143">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a6df3-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a6df3-144">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="a6df3-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a6df3-145">Inputobject <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="a6df3-145">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="a6df3-146">`Location <String>`: Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="a6df3-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="a6df3-147">`[Kind <String>]`: Art der Ressource.</span><span class="sxs-lookup"><span data-stu-id="a6df3-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="a6df3-148">`[Tag <IResourceTags>]`: Ressourcenkategorien.</span><span class="sxs-lookup"><span data-stu-id="a6df3-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="a6df3-149">`[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a6df3-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="a6df3-150">`[Capacity <Int32?>]`: Aktuelle Anzahl der Instanzen, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a6df3-150">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="a6df3-151">`[FreeOfferExpirationTime <DateTime?>]`: Der Zeitpunkt, zu dem das ﻿kostenlose Angebot der Serverfarm abläuft.</span><span class="sxs-lookup"><span data-stu-id="a6df3-151">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="a6df3-152">`[HostingEnvironmentProfileId <String>]`: Ressourcen-ID der APP-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="a6df3-152">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="a6df3-153">`[HyperV <Boolean?>]`: Wenn der Hyper-V-Container-App-Service Plan <code>true</code> , <code>false</code> andernfalls.</span><span class="sxs-lookup"><span data-stu-id="a6df3-153">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="a6df3-154">`[IsSpot <Boolean?>]`: Wenn <code>true</code> dieser APP-Service Plan über Spot-Instances verfügt.</span><span class="sxs-lookup"><span data-stu-id="a6df3-154">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="a6df3-155">`[IsXenon <Boolean?>]`: Veraltet: Wenn der Hyper-V-Container-App-Service Plan <code>true</code> , <code>false</code> andernfalls.</span><span class="sxs-lookup"><span data-stu-id="a6df3-155">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="a6df3-156">`[MaximumElasticWorkerCount <Int32?>]`: Maximale Anzahl der insgesamt für diesen ElasticScaleEnabled-App-Service Plan zulässigen Arbeitskräfte</span><span class="sxs-lookup"><span data-stu-id="a6df3-156">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="a6df3-157">`[PerSiteScaling <Boolean?>]`: Wenn <code>true</code> apps, die diesem app-Service Plan zugewiesen sind, unabhängig voneinander skaliert werden können.</span><span class="sxs-lookup"><span data-stu-id="a6df3-157">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="a6df3-158">Wenn <code>false</code> die diesem app-Service Plan zugewiesenen apps auf alle Instanzen des Plans skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="a6df3-158">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="a6df3-159">`[Reserved <Boolean?>]`: Wenn der Linux-APP <code>true</code> -Service Plan, <code>false</code> andernfalls.</span><span class="sxs-lookup"><span data-stu-id="a6df3-159">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="a6df3-160">`[SkuCapability <ICapability[]>]`: Funktionen der SKU, beispielsweise ist Traffic Manager aktiviert?</span><span class="sxs-lookup"><span data-stu-id="a6df3-160">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="a6df3-161">`[Name <String>]`: Name der SKU-Funktion.</span><span class="sxs-lookup"><span data-stu-id="a6df3-161">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="a6df3-162">`[Reason <String>]`: Grund für die SKU-Funktion.</span><span class="sxs-lookup"><span data-stu-id="a6df3-162">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="a6df3-163">`[Value <String>]`: Wert der SKU-Funktion.</span><span class="sxs-lookup"><span data-stu-id="a6df3-163">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="a6df3-164">`[SkuCapacityDefault <Int32?>]`: Standardanzahl von Arbeitskräften für diese APP-Service Plan-SKU.</span><span class="sxs-lookup"><span data-stu-id="a6df3-164">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="a6df3-165">`[SkuCapacityMaximum <Int32?>]`: Maximale Anzahl von Arbeitskräften für diese APP-Service Plan-SKU.</span><span class="sxs-lookup"><span data-stu-id="a6df3-165">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="a6df3-166">`[SkuCapacityMinimum <Int32?>]`: Mindestanzahl von Arbeitskräften für diese APP-Service Plan-SKU.</span><span class="sxs-lookup"><span data-stu-id="a6df3-166">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="a6df3-167">`[SkuCapacityScaleType <String>]`: Verfügbare Skalierungs Konfigurationen für einen app-Service Plan.</span><span class="sxs-lookup"><span data-stu-id="a6df3-167">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="a6df3-168">`[SkuFamily <String>]`: Familiencode der Ressourcen-SKU.</span><span class="sxs-lookup"><span data-stu-id="a6df3-168">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="a6df3-169">`[SkuLocation <String[]>]`: Speicherorte der SKU.</span><span class="sxs-lookup"><span data-stu-id="a6df3-169">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="a6df3-170">`[SkuName <String>]`: Name der Ressourcen-SKU.</span><span class="sxs-lookup"><span data-stu-id="a6df3-170">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="a6df3-171">`[SkuSize <String>]`: Size-Bezeichner der Ressourcen-SKU.</span><span class="sxs-lookup"><span data-stu-id="a6df3-171">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="a6df3-172">`[SkuTier <String>]`: Dienstebene der Ressourcen-SKU.</span><span class="sxs-lookup"><span data-stu-id="a6df3-172">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="a6df3-173">`[SpotExpirationTime <DateTime?>]`: Der Zeitpunkt, zu dem die Serverfarm abläuft.</span><span class="sxs-lookup"><span data-stu-id="a6df3-173">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="a6df3-174">Nur gültig, wenn es sich um eine Spot Serverfarm handelt.</span><span class="sxs-lookup"><span data-stu-id="a6df3-174">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="a6df3-175">`[TargetWorkerCount <Int32?>]`: Skalieren der Worker-Anzahl</span><span class="sxs-lookup"><span data-stu-id="a6df3-175">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="a6df3-176">`[TargetWorkerSizeId <Int32?>]`: Skalierung der Worker-Größen-ID.</span><span class="sxs-lookup"><span data-stu-id="a6df3-176">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="a6df3-177">`[WorkerTierName <String>]`: Zielarbeitsebene, die dem App-Service Plan zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="a6df3-177">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="a6df3-178">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a6df3-178">RELATED LINKS</span></span>

