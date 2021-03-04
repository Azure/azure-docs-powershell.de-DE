---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: a3180cd693ae4c234656ba5d0812900ce8c308b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942664"
---
# <span data-ttu-id="a6932-101">New-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="a6932-101">New-AzCustomProvider</span></span>

## <span data-ttu-id="a6932-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6932-102">SYNOPSIS</span></span>
<span data-ttu-id="a6932-103">Erstellt oder aktualisiert den benutzerdefinierten Ressourcenanbieter.</span><span class="sxs-lookup"><span data-stu-id="a6932-103">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="a6932-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6932-104">SYNTAX</span></span>

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a6932-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a6932-105">DESCRIPTION</span></span>
<span data-ttu-id="a6932-106">Erstellt oder aktualisiert den benutzerdefinierten Ressourcenanbieter.</span><span class="sxs-lookup"><span data-stu-id="a6932-106">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="a6932-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a6932-107">EXAMPLES</span></span>

### <span data-ttu-id="a6932-108">Beispiel 1: Erstellen eines benutzerdefinierten Anbieters</span><span class="sxs-lookup"><span data-stu-id="a6932-108">Example 1: Create a custom provider</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="a6932-109">Erstellen eines benutzerdefinierten Ressourcenanbieters</span><span class="sxs-lookup"><span data-stu-id="a6932-109">Create a custom resource provider</span></span>

### <span data-ttu-id="a6932-110">Beispiel 2: Erstellen eines benutzerdefinierten Anbieters mit Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="a6932-110">Example 2: Create a custom provider with associations</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="a6932-111">Erstellen Sie einen benutzerdefinierten Anbieter mit einer Route für benutzerdefinierte Anbieterzuordnungen.</span><span class="sxs-lookup"><span data-stu-id="a6932-111">Create a custom provider, with a route for Custom provider associations.</span></span>

## <span data-ttu-id="a6932-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a6932-112">PARAMETERS</span></span>

### <span data-ttu-id="a6932-113">-Aktion</span><span class="sxs-lookup"><span data-stu-id="a6932-113">-Action</span></span>
<span data-ttu-id="a6932-114">Eine Liste der Aktionen, die vom benutzerdefinierten Ressourcenanbieter implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="a6932-114">A list of actions that the custom resource provider implements.</span></span>
<span data-ttu-id="a6932-115">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu ACTION-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a6932-115">To construct, see NOTES section for ACTION properties and create a hash table.</span></span>

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

### <span data-ttu-id="a6932-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6932-116">-AsJob</span></span>
<span data-ttu-id="a6932-117">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="a6932-117">Run the command as a job</span></span>

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

### <span data-ttu-id="a6932-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6932-118">-DefaultProfile</span></span>
<span data-ttu-id="a6932-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a6932-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6932-120">-Location</span><span class="sxs-lookup"><span data-stu-id="a6932-120">-Location</span></span>
<span data-ttu-id="a6932-121">Ressourcenspeicherort</span><span class="sxs-lookup"><span data-stu-id="a6932-121">Resource location</span></span>

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

### <span data-ttu-id="a6932-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a6932-122">-Name</span></span>
<span data-ttu-id="a6932-123">Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="a6932-123">The name of the resource provider.</span></span>

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

### <span data-ttu-id="a6932-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a6932-124">-NoWait</span></span>
<span data-ttu-id="a6932-125">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="a6932-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a6932-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6932-126">-ResourceGroupName</span></span>
<span data-ttu-id="a6932-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a6932-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="a6932-128">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a6932-128">-ResourceType</span></span>
<span data-ttu-id="a6932-129">Eine Liste der Ressourcentypen, die vom benutzerdefinierten Ressourcenanbieter implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="a6932-129">A list of resource types that the custom resource provider implements.</span></span>
<span data-ttu-id="a6932-130">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN für RESSOURCENTYP-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a6932-130">To construct, see NOTES section for RESOURCETYPE properties and create a hash table.</span></span>

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

### <span data-ttu-id="a6932-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a6932-131">-SubscriptionId</span></span>
<span data-ttu-id="a6932-132">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="a6932-132">The Azure subscription ID.</span></span>
<span data-ttu-id="a6932-133">Dies ist eine GUID-formatierte Zeichenfolge (z. B. 000000000-0000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="a6932-133">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="a6932-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="a6932-134">-Tag</span></span>
<span data-ttu-id="a6932-135">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="a6932-135">Resource tags</span></span>

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

### <span data-ttu-id="a6932-136">-Überprüfung</span><span class="sxs-lookup"><span data-stu-id="a6932-136">-Validation</span></span>
<span data-ttu-id="a6932-137">Eine Liste der Überprüfungen, die für die Anforderungen des benutzerdefinierten Ressourcenanbieters ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a6932-137">A list of validations to run on the custom resource provider's requests.</span></span>
<span data-ttu-id="a6932-138">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN für GÜLTIGKEITSPRÜFUNGseigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a6932-138">To construct, see NOTES section for VALIDATION properties and create a hash table.</span></span>

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

### <span data-ttu-id="a6932-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a6932-139">-Confirm</span></span>
<span data-ttu-id="a6932-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a6932-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6932-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6932-141">-WhatIf</span></span>
<span data-ttu-id="a6932-142">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6932-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6932-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6932-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6932-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6932-144">CommonParameters</span></span>
<span data-ttu-id="a6932-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6932-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6932-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6932-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6932-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a6932-147">INPUTS</span></span>

## <span data-ttu-id="a6932-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a6932-148">OUTPUTS</span></span>

### <span data-ttu-id="a6932-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="a6932-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="a6932-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a6932-150">NOTES</span></span>

<span data-ttu-id="a6932-151">ALIASE</span><span class="sxs-lookup"><span data-stu-id="a6932-151">ALIASES</span></span>

<span data-ttu-id="a6932-152">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="a6932-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a6932-153">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="a6932-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a6932-154">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a6932-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a6932-155">ACTION <ICustomRpActionRouteDefinition[]>: Eine Liste der Aktionen, die vom benutzerdefinierten Ressourcenanbieter implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="a6932-155">ACTION <ICustomRpActionRouteDefinition[]>: A list of actions that the custom resource provider implements.</span></span>
  - <span data-ttu-id="a6932-156">`Endpoint <String>`: Der Routendefinitionsendpunkt-URI, an den vom benutzerdefinierten Ressourcenanbieter Proxyanforderungen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="a6932-156">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="a6932-157">Dies kann in Form eines flachen URI (z. B. ' ') oder als Route über einen Pfad https://testendpoint/ angegeben werden (z. B. ' https://testendpoint/{requestPath} ')</span><span class="sxs-lookup"><span data-stu-id="a6932-157">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="a6932-158">`Name <String>`: Der Name der Routendefinition.</span><span class="sxs-lookup"><span data-stu-id="a6932-158">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="a6932-159">Dies wird der Name der ARM-Erweiterung (z. B. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span><span class="sxs-lookup"><span data-stu-id="a6932-159">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="a6932-160">`[RoutingType <ActionRouting?>]`: Die Routingtypen, die für Aktionsanforderungen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a6932-160">`[RoutingType <ActionRouting?>]`: The routing types that are supported for action requests.</span></span>

<span data-ttu-id="a6932-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: Eine Liste der Ressourcentypen, die vom benutzerdefinierten Ressourcenanbieter implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="a6932-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: A list of resource types that the custom resource provider implements.</span></span>
  - <span data-ttu-id="a6932-162">`Endpoint <String>`: Der Routendefinitionsendpunkt-URI, an den vom benutzerdefinierten Ressourcenanbieter Proxyanforderungen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="a6932-162">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="a6932-163">Dies kann in Form eines flachen URI (z. B. ' ') oder als Route über einen Pfad https://testendpoint/ angegeben werden (z. B. ' https://testendpoint/{requestPath} ')</span><span class="sxs-lookup"><span data-stu-id="a6932-163">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="a6932-164">`Name <String>`: Der Name der Routendefinition.</span><span class="sxs-lookup"><span data-stu-id="a6932-164">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="a6932-165">Dies wird der Name der ARM-Erweiterung (z. B. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span><span class="sxs-lookup"><span data-stu-id="a6932-165">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="a6932-166">`[RoutingType <ResourceTypeRouting?>]`: Die Routingtypen, die für Ressourcenanforderungen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a6932-166">`[RoutingType <ResourceTypeRouting?>]`: The routing types that are supported for resource requests.</span></span>

<span data-ttu-id="a6932-167">VALIDATION <ICustomRpValidations[]>: Eine Liste der Überprüfungen, die für die Anforderungen des benutzerdefinierten Ressourcenanbieters ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a6932-167">VALIDATION <ICustomRpValidations[]>: A list of validations to run on the custom resource provider's requests.</span></span>
  - <span data-ttu-id="a6932-168">`Specification <String>`: Ein Link zur Gültigkeitsprüfungsspezifikation.</span><span class="sxs-lookup"><span data-stu-id="a6932-168">`Specification <String>`: A link to the validation specification.</span></span> <span data-ttu-id="a6932-169">Die Spezifikation muss auf einer raw.githubusercontent.com.</span><span class="sxs-lookup"><span data-stu-id="a6932-169">The specification must be hosted on raw.githubusercontent.com.</span></span>
  - <span data-ttu-id="a6932-170">`[ValidationType <ValidationType?>]`: Der Typ der Überprüfung, die für eine übereinstimmende Anforderung ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a6932-170">`[ValidationType <ValidationType?>]`: The type of validation to run against a matching request.</span></span>

## <span data-ttu-id="a6932-171">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a6932-171">RELATED LINKS</span></span>

