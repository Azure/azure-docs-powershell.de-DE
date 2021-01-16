---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: 7f91fee2e8cc772be291662af325fd87edebdfd9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297575"
---
# <span data-ttu-id="c505d-101">New-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="c505d-101">New-AzCustomProvider</span></span>

## <span data-ttu-id="c505d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c505d-102">SYNOPSIS</span></span>
<span data-ttu-id="c505d-103">Erstellt oder aktualisiert den benutzerdefinierten Ressourcenanbieter.</span><span class="sxs-lookup"><span data-stu-id="c505d-103">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="c505d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c505d-104">SYNTAX</span></span>

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c505d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c505d-105">DESCRIPTION</span></span>
<span data-ttu-id="c505d-106">Erstellt oder aktualisiert den benutzerdefinierten Ressourcenanbieter.</span><span class="sxs-lookup"><span data-stu-id="c505d-106">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="c505d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c505d-107">EXAMPLES</span></span>

### <span data-ttu-id="c505d-108">Beispiel 1: Erstellen eines benutzerdefinierten Anbieters</span><span class="sxs-lookup"><span data-stu-id="c505d-108">Example 1: Create a custom provider</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="c505d-109">Erstellen eines benutzerdefinierten Ressourcenanbieters</span><span class="sxs-lookup"><span data-stu-id="c505d-109">Create a custom resource provider</span></span>

### <span data-ttu-id="c505d-110">Beispiel 2: Erstellen eines benutzerdefinierten Anbieters mit Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="c505d-110">Example 2: Create a custom provider with associations</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="c505d-111">Erstellen Sie einen benutzerdefinierten Anbieter mit einer Route für benutzerdefinierte Anbieterzuordnungen.</span><span class="sxs-lookup"><span data-stu-id="c505d-111">Create a custom provider, with a route for Custom provider associations.</span></span>

## <span data-ttu-id="c505d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c505d-112">PARAMETERS</span></span>

### <span data-ttu-id="c505d-113">-Aktion</span><span class="sxs-lookup"><span data-stu-id="c505d-113">-Action</span></span>
<span data-ttu-id="c505d-114">Eine Liste der Aktionen, die vom benutzerdefinierten Ressourcenanbieter implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="c505d-114">A list of actions that the custom resource provider implements.</span></span>
<span data-ttu-id="c505d-115">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c505d-115">To construct, see NOTES section for ACTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpActionRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c505d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c505d-116">-AsJob</span></span>
<span data-ttu-id="c505d-117">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="c505d-117">Run the command as a job</span></span>

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

### <span data-ttu-id="c505d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c505d-118">-DefaultProfile</span></span>
<span data-ttu-id="c505d-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c505d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c505d-120">-Location</span><span class="sxs-lookup"><span data-stu-id="c505d-120">-Location</span></span>
<span data-ttu-id="c505d-121">Ressourcenspeicherort</span><span class="sxs-lookup"><span data-stu-id="c505d-121">Resource location</span></span>

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

### <span data-ttu-id="c505d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c505d-122">-Name</span></span>
<span data-ttu-id="c505d-123">Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="c505d-123">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c505d-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c505d-124">-NoWait</span></span>
<span data-ttu-id="c505d-125">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="c505d-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c505d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c505d-126">-ResourceGroupName</span></span>
<span data-ttu-id="c505d-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c505d-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="c505d-128">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c505d-128">-ResourceType</span></span>
<span data-ttu-id="c505d-129">Eine Liste der Ressourcentypen, die vom benutzerdefinierten Ressourcenanbieter implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="c505d-129">A list of resource types that the custom resource provider implements.</span></span>
<span data-ttu-id="c505d-130">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c505d-130">To construct, see NOTES section for RESOURCETYPE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpResourceTypeRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c505d-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c505d-131">-SubscriptionId</span></span>
<span data-ttu-id="c505d-132">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="c505d-132">The Azure subscription ID.</span></span>
<span data-ttu-id="c505d-133">Dies ist eine GUID-formatierte Zeichenfolge (z. B. 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="c505d-133">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="c505d-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="c505d-134">-Tag</span></span>
<span data-ttu-id="c505d-135">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="c505d-135">Resource tags</span></span>

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

### <span data-ttu-id="c505d-136">-Überprüfung</span><span class="sxs-lookup"><span data-stu-id="c505d-136">-Validation</span></span>
<span data-ttu-id="c505d-137">Eine Liste der Überprüfungen, die für Anforderungen des benutzerdefinierten Ressourcenanbieters ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c505d-137">A list of validations to run on the custom resource provider's requests.</span></span>
<span data-ttu-id="c505d-138">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c505d-138">To construct, see NOTES section for VALIDATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpValidations[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c505d-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c505d-139">-Confirm</span></span>
<span data-ttu-id="c505d-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c505d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c505d-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c505d-141">-WhatIf</span></span>
<span data-ttu-id="c505d-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c505d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c505d-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c505d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c505d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c505d-144">CommonParameters</span></span>
<span data-ttu-id="c505d-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c505d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c505d-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c505d-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c505d-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c505d-147">INPUTS</span></span>

## <span data-ttu-id="c505d-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c505d-148">OUTPUTS</span></span>

### <span data-ttu-id="c505d-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="c505d-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="c505d-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c505d-150">NOTES</span></span>

<span data-ttu-id="c505d-151">ALIASE</span><span class="sxs-lookup"><span data-stu-id="c505d-151">ALIASES</span></span>

<span data-ttu-id="c505d-152">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="c505d-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c505d-153">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c505d-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c505d-154">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c505d-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c505d-155">ACTION <ICustomRpActionRouteDefinition[]>: Eine Liste von Aktionen, die vom benutzerdefinierten Ressourcenanbieter implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="c505d-155">ACTION <ICustomRpActionRouteDefinition[]>: A list of actions that the custom resource provider implements.</span></span>
  - <span data-ttu-id="c505d-156">`Endpoint <String>`: Der Endpunkt für die Routendefinition, an den der benutzerdefinierte Ressourcenanbieter Proxyanforderungen anfordert.</span><span class="sxs-lookup"><span data-stu-id="c505d-156">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="c505d-157">Dies kann in Form eines flachen URI (z. B. ' ') oder als Route über einen Pfad https://testendpoint/ angegeben werden (z. B. ' https://testendpoint/{requestPath} ')</span><span class="sxs-lookup"><span data-stu-id="c505d-157">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="c505d-158">`Name <String>`: Der Name der Routendefinition.</span><span class="sxs-lookup"><span data-stu-id="c505d-158">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="c505d-159">Dies wird der Name für die ARM-Erweiterung (z. B. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span><span class="sxs-lookup"><span data-stu-id="c505d-159">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="c505d-160">`[RoutingType <ActionRouting?>]`: Die Routingtypen, die für Aktionsanforderungen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="c505d-160">`[RoutingType <ActionRouting?>]`: The routing types that are supported for action requests.</span></span>

<span data-ttu-id="c505d-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: Eine Liste der Ressourcentypen, die vom benutzerdefinierten Ressourcenanbieter implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="c505d-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: A list of resource types that the custom resource provider implements.</span></span>
  - <span data-ttu-id="c505d-162">`Endpoint <String>`: Der Endpunkt für die Routendefinition, an den der benutzerdefinierte Ressourcenanbieter Proxyanforderungen anfordert.</span><span class="sxs-lookup"><span data-stu-id="c505d-162">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="c505d-163">Dies kann in Form eines flachen URI (z. B. ' ') oder als Route über einen Pfad https://testendpoint/ angegeben werden (z. B. ' https://testendpoint/{requestPath} ')</span><span class="sxs-lookup"><span data-stu-id="c505d-163">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="c505d-164">`Name <String>`: Der Name der Routendefinition.</span><span class="sxs-lookup"><span data-stu-id="c505d-164">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="c505d-165">Dies wird der Name für die ARM-Erweiterung (z. B. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span><span class="sxs-lookup"><span data-stu-id="c505d-165">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="c505d-166">`[RoutingType <ResourceTypeRouting?>]`: Die Routingtypen, die für Ressourcenanforderungen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="c505d-166">`[RoutingType <ResourceTypeRouting?>]`: The routing types that are supported for resource requests.</span></span>

<span data-ttu-id="c505d-167">VALIDATION <ICustomRpValidations[]>: Eine Liste der Überprüfungen, die für Anforderungen des benutzerdefinierten Ressourcenanbieters ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c505d-167">VALIDATION <ICustomRpValidations[]>: A list of validations to run on the custom resource provider's requests.</span></span>
  - <span data-ttu-id="c505d-168">`Specification <String>`: Eine Verknüpfung zur Gültigkeitsprüfungsspezifikation.</span><span class="sxs-lookup"><span data-stu-id="c505d-168">`Specification <String>`: A link to the validation specification.</span></span> <span data-ttu-id="c505d-169">Die Spezifikation muss auf einem raw.githubusercontent.com.</span><span class="sxs-lookup"><span data-stu-id="c505d-169">The specification must be hosted on raw.githubusercontent.com.</span></span>
  - <span data-ttu-id="c505d-170">`[ValidationType <ValidationType?>]`: Der Typ der Überprüfung, die für eine übereinstimmende Anforderung ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c505d-170">`[ValidationType <ValidationType?>]`: The type of validation to run against a matching request.</span></span>

## <span data-ttu-id="c505d-171">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c505d-171">RELATED LINKS</span></span>

