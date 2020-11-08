---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: 7f91fee2e8cc772be291662af325fd87edebdfd9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174806"
---
# <span data-ttu-id="76910-101">New-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="76910-101">New-AzCustomProvider</span></span>

## <span data-ttu-id="76910-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="76910-102">SYNOPSIS</span></span>
<span data-ttu-id="76910-103">Erstellt oder aktualisiert den benutzerdefinierten Ressourcenanbieter.</span><span class="sxs-lookup"><span data-stu-id="76910-103">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="76910-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="76910-104">SYNTAX</span></span>

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="76910-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76910-105">DESCRIPTION</span></span>
<span data-ttu-id="76910-106">Erstellt oder aktualisiert den benutzerdefinierten Ressourcenanbieter.</span><span class="sxs-lookup"><span data-stu-id="76910-106">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="76910-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="76910-107">EXAMPLES</span></span>

### <span data-ttu-id="76910-108">Beispiel 1: Erstellen eines benutzerdefinierten Anbieters</span><span class="sxs-lookup"><span data-stu-id="76910-108">Example 1: Create a custom provider</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="76910-109">Erstellen eines benutzerdefinierten Ressourcenanbieters</span><span class="sxs-lookup"><span data-stu-id="76910-109">Create a custom resource provider</span></span>

### <span data-ttu-id="76910-110">Beispiel 2: Erstellen eines benutzerdefinierten Anbieters mit Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="76910-110">Example 2: Create a custom provider with associations</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="76910-111">Erstellen Sie einen benutzerdefinierten Anbieter mit einer Route für benutzerdefinierte Anbieter Zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="76910-111">Create a custom provider, with a route for Custom provider associations.</span></span>

## <span data-ttu-id="76910-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="76910-112">PARAMETERS</span></span>

### <span data-ttu-id="76910-113">– Aktion</span><span class="sxs-lookup"><span data-stu-id="76910-113">-Action</span></span>
<span data-ttu-id="76910-114">Eine Liste der Aktionen, die der benutzerdefinierte Ressourcenanbieter implementiert.</span><span class="sxs-lookup"><span data-stu-id="76910-114">A list of actions that the custom resource provider implements.</span></span>
<span data-ttu-id="76910-115">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Aktionseigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="76910-115">To construct, see NOTES section for ACTION properties and create a hash table.</span></span>

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

### <span data-ttu-id="76910-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76910-116">-AsJob</span></span>
<span data-ttu-id="76910-117">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="76910-117">Run the command as a job</span></span>

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

### <span data-ttu-id="76910-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76910-118">-DefaultProfile</span></span>
<span data-ttu-id="76910-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="76910-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76910-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="76910-120">-Location</span></span>
<span data-ttu-id="76910-121">Ressourcen Standort</span><span class="sxs-lookup"><span data-stu-id="76910-121">Resource location</span></span>

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

### <span data-ttu-id="76910-122">-Name</span><span class="sxs-lookup"><span data-stu-id="76910-122">-Name</span></span>
<span data-ttu-id="76910-123">Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="76910-123">The name of the resource provider.</span></span>

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

### <span data-ttu-id="76910-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="76910-124">-NoWait</span></span>
<span data-ttu-id="76910-125">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="76910-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="76910-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76910-126">-ResourceGroupName</span></span>
<span data-ttu-id="76910-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="76910-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="76910-128">-</span><span class="sxs-lookup"><span data-stu-id="76910-128">-ResourceType</span></span>
<span data-ttu-id="76910-129">Eine Liste der Ressourcentypen, die vom benutzerdefinierten Ressourcenanbieter implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="76910-129">A list of resource types that the custom resource provider implements.</span></span>
<span data-ttu-id="76910-130">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Eigenschaften von "Eigenschaften" und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="76910-130">To construct, see NOTES section for RESOURCETYPE properties and create a hash table.</span></span>

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

### <span data-ttu-id="76910-131">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="76910-131">-SubscriptionId</span></span>
<span data-ttu-id="76910-132">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="76910-132">The Azure subscription ID.</span></span>
<span data-ttu-id="76910-133">Hierbei handelt es sich um eine GUID-formatierte Zeichenfolge (z.b. 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="76910-133">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="76910-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="76910-134">-Tag</span></span>
<span data-ttu-id="76910-135">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="76910-135">Resource tags</span></span>

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

### <span data-ttu-id="76910-136">-Validierung</span><span class="sxs-lookup"><span data-stu-id="76910-136">-Validation</span></span>
<span data-ttu-id="76910-137">Eine Liste der Validierungen, die für die Anforderungen des benutzerdefinierten Ressourcenanbieters ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="76910-137">A list of validations to run on the custom resource provider's requests.</span></span>
<span data-ttu-id="76910-138">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Überprüfungseigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="76910-138">To construct, see NOTES section for VALIDATION properties and create a hash table.</span></span>

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

### <span data-ttu-id="76910-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="76910-139">-Confirm</span></span>
<span data-ttu-id="76910-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76910-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76910-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76910-141">-WhatIf</span></span>
<span data-ttu-id="76910-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76910-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76910-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76910-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76910-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76910-144">CommonParameters</span></span>
<span data-ttu-id="76910-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76910-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76910-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76910-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76910-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="76910-147">INPUTS</span></span>

## <span data-ttu-id="76910-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="76910-148">OUTPUTS</span></span>

### <span data-ttu-id="76910-149">Microsoft. Azure. PowerShell. Cmdlets. CustomProviders. Models. Api20180901Preview. ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="76910-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="76910-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="76910-150">NOTES</span></span>

<span data-ttu-id="76910-151">Aliase</span><span class="sxs-lookup"><span data-stu-id="76910-151">ALIASES</span></span>

<span data-ttu-id="76910-152">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="76910-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="76910-153">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="76910-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="76910-154">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="76910-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="76910-155">Action <ICustomRpActionRouteDefinition [] >: eine Liste der Aktionen, die vom benutzerdefinierten Ressourcenanbieter implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="76910-155">ACTION <ICustomRpActionRouteDefinition[]>: A list of actions that the custom resource provider implements.</span></span>
  - <span data-ttu-id="76910-156">`Endpoint <String>`: Der Endpunkt-URI für die Routendefinition, an den der benutzerdefinierte Ressourcenanbieter Proxyanforderungen stellt.</span><span class="sxs-lookup"><span data-stu-id="76910-156">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="76910-157">Dies kann in Form eines flachen URIs erfolgen (z.b. ' https://testendpoint/ ') oder es kann angegeben werden, dass es über einen Pfad weitergeleitet werden soll (z.b. ' https://testendpoint/{requestPath} ').</span><span class="sxs-lookup"><span data-stu-id="76910-157">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="76910-158">`Name <String>`: Der Name der Routendefinition.</span><span class="sxs-lookup"><span data-stu-id="76910-158">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="76910-159">Dies wird zum Namen für die Erweiterung des Arms (z.b. "/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{Name}").</span><span class="sxs-lookup"><span data-stu-id="76910-159">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="76910-160">`[RoutingType <ActionRouting?>]`: Die Routing Typen, die für Aktionsanforderungen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="76910-160">`[RoutingType <ActionRouting?>]`: The routing types that are supported for action requests.</span></span>

<span data-ttu-id="76910-161">Ressourcen <ICustomRpResourceTypeRouteDefinition [] >: eine Liste der Ressourcentypen, die vom benutzerdefinierten Ressourcenanbieter implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="76910-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: A list of resource types that the custom resource provider implements.</span></span>
  - <span data-ttu-id="76910-162">`Endpoint <String>`: Der Endpunkt-URI für die Routendefinition, an den der benutzerdefinierte Ressourcenanbieter Proxyanforderungen stellt.</span><span class="sxs-lookup"><span data-stu-id="76910-162">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="76910-163">Dies kann in Form eines flachen URIs erfolgen (z.b. ' https://testendpoint/ ') oder es kann angegeben werden, dass es über einen Pfad weitergeleitet werden soll (z.b. ' https://testendpoint/{requestPath} ').</span><span class="sxs-lookup"><span data-stu-id="76910-163">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="76910-164">`Name <String>`: Der Name der Routendefinition.</span><span class="sxs-lookup"><span data-stu-id="76910-164">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="76910-165">Dies wird zum Namen für die Erweiterung des Arms (z.b. "/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{Name}").</span><span class="sxs-lookup"><span data-stu-id="76910-165">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="76910-166">`[RoutingType <ResourceTypeRouting?>]`: Die Routing Typen, die für Ressourcenanforderungen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="76910-166">`[RoutingType <ResourceTypeRouting?>]`: The routing types that are supported for resource requests.</span></span>

<span data-ttu-id="76910-167">Validation <ICustomRpValidations [] >: eine Liste der Validierungen, die für die Anforderungen des benutzerdefinierten Ressourcenanbieters ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="76910-167">VALIDATION <ICustomRpValidations[]>: A list of validations to run on the custom resource provider's requests.</span></span>
  - <span data-ttu-id="76910-168">`Specification <String>`: Ein Link zur Gültigkeits Prüfungs Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="76910-168">`Specification <String>`: A link to the validation specification.</span></span> <span data-ttu-id="76910-169">Die Spezifikation muss auf RAW.githubusercontent.com gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="76910-169">The specification must be hosted on raw.githubusercontent.com.</span></span>
  - <span data-ttu-id="76910-170">`[ValidationType <ValidationType?>]`: Die Art der Validierung, die für eine übereinstimmende Anforderung ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="76910-170">`[ValidationType <ValidationType?>]`: The type of validation to run against a matching request.</span></span>

## <span data-ttu-id="76910-171">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="76910-171">RELATED LINKS</span></span>

