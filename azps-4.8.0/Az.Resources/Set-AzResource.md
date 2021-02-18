---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
ms.openlocfilehash: 82e06a4736a613111efac452eb1fced2713dc470
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415749"
---
# <span data-ttu-id="5410a-101">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="5410a-101">Set-AzResource</span></span>

## <span data-ttu-id="5410a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5410a-102">SYNOPSIS</span></span>
<span data-ttu-id="5410a-103">Ändert eine Ressource.</span><span class="sxs-lookup"><span data-stu-id="5410a-103">Modifies a resource.</span></span>

## <span data-ttu-id="5410a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5410a-104">SYNTAX</span></span>

### <span data-ttu-id="5410a-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="5410a-105">ByResourceId (Default)</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5410a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5410a-106">ByInputObject</span></span>
```
Set-AzResource -InputObject <PSResource> [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5410a-107">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="5410a-107">BySubscriptionLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5410a-108">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="5410a-108">ByTenantLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5410a-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5410a-109">DESCRIPTION</span></span>
<span data-ttu-id="5410a-110">Das **Cmdlet "Set-AzResource"** ändert eine vorhandene Azure-Ressource.</span><span class="sxs-lookup"><span data-stu-id="5410a-110">The **Set-AzResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="5410a-111">Geben Sie eine Ressource an, die nach Name und Typ oder ID geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5410a-111">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="5410a-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5410a-112">EXAMPLES</span></span>

### <span data-ttu-id="5410a-113">Beispiel 1: Ändern einer Ressource</span><span class="sxs-lookup"><span data-stu-id="5410a-113">Example 1: Modify a resource</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceType Microsoft.Web/sites -ResourceGroupName ResourceGroup11 -ResourceName ContosoSite
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzResource -Force
```

<span data-ttu-id="5410a-114">Der erste Befehl ruft die Ressource "ContosoSite" mithilfe des Cmdlets "Get-AzResource" ab und speichert sie dann in $Resource Variable.</span><span class="sxs-lookup"><span data-stu-id="5410a-114">The first command gets the resource named ContosoSite by using the Get-AzResource cmdlet, and then stores it in the $Resource variable.</span></span>
<span data-ttu-id="5410a-115">Der zweite Befehl ändert die Eigenschaft $Resource.</span><span class="sxs-lookup"><span data-stu-id="5410a-115">The second command modifies a property of $Resource.</span></span>
<span data-ttu-id="5410a-116">Der letzte Befehl aktualisiert die Ressource so, dass sie $Resource.</span><span class="sxs-lookup"><span data-stu-id="5410a-116">The final command updates the resource to match $Resource.</span></span>

### <span data-ttu-id="5410a-117">Beispiel 2: Ändern aller Ressourcen in einer bestimmten Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5410a-117">Example 2: Modify all resources in a given resource group</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceGroupName testrg
PS C:\> $Resource | ForEach-Object { $_.Tags.Add("testkey", "testval") }
PS C:\> $Resource | Set-AzResource -Force

Name              : kv-test
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.KeyVault/vaults/kv-test
ResourceName      : kv-test
ResourceType      : Microsoft.KeyVault/vaults
ResourceGroupName : testrg
Location          : westus
SubscriptionId    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags              : {testrgkey, key}
Properties        : @{}

Name              : testresource
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Providers.Test/statefulResources/testresource
ResourceName      : testresource
ResourceType      : Providers.Test/statefulResources
ResourceGroupName : testrg
Location          : West US 2
SubscriptionId    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags              : {testrgkey, anothertesttag}
Properties        : @{key=value}
Sku               : @{name=A0}
```

<span data-ttu-id="5410a-118">Der erste Befehl ruft die Ressourcen in der Ressourcengruppe "testrg" ab und speichert sie dann in der $Resource Variable.</span><span class="sxs-lookup"><span data-stu-id="5410a-118">The first command gets the resources in the testrg resource group, and then stores them in the $Resource variable.</span></span>

<span data-ttu-id="5410a-119">Mit dem zweiten Befehl wird jede dieser Ressourcen in der Ressourcengruppe durch iteriert und ihnen ein neues Tag hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="5410a-119">The second command iterates over each of these resources in the resource group and adds a new tag to them.</span></span>

<span data-ttu-id="5410a-120">Der letzte Befehl aktualisiert jede dieser Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="5410a-120">The final command updates each of these resources.</span></span>

## <span data-ttu-id="5410a-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5410a-121">PARAMETERS</span></span>

### <span data-ttu-id="5410a-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5410a-122">-ApiVersion</span></span>
<span data-ttu-id="5410a-123">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="5410a-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="5410a-124">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="5410a-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="5410a-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5410a-125">-AsJob</span></span>
<span data-ttu-id="5410a-126">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5410a-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5410a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5410a-127">-DefaultProfile</span></span>
<span data-ttu-id="5410a-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5410a-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5410a-129">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="5410a-129">-ExtensionResourceName</span></span>
<span data-ttu-id="5410a-130">Gibt den Namen einer Erweiterungsressource für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="5410a-130">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="5410a-131">Um beispielsweise eine Datenbank anzugeben, verwenden Sie das folgende Format: Name der `/` Serverdatenbank</span><span class="sxs-lookup"><span data-stu-id="5410a-131">For instance, to specify a database, use the following format: server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5410a-132">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="5410a-132">-ExtensionResourceType</span></span>
<span data-ttu-id="5410a-133">Gibt den Ressourcentyp für eine Erweiterungsressource an.</span><span class="sxs-lookup"><span data-stu-id="5410a-133">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="5410a-134">Wenn es sich bei der Erweiterungsressource beispielsweise um eine Datenbank handelt, geben Sie Folgendes an: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="5410a-134">For instance, if the extension resource is a database specify the following: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5410a-135">-Force</span><span class="sxs-lookup"><span data-stu-id="5410a-135">-Force</span></span>
<span data-ttu-id="5410a-136">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="5410a-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5410a-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5410a-137">-InputObject</span></span>
<span data-ttu-id="5410a-138">Die Objektdarstellung der zu aktualisierende Ressource.</span><span class="sxs-lookup"><span data-stu-id="5410a-138">The object representation of the resource to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5410a-139">-Kind</span><span class="sxs-lookup"><span data-stu-id="5410a-139">-Kind</span></span>
<span data-ttu-id="5410a-140">Gibt die Ressourcentyp für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="5410a-140">Specifies the resource kind for the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5410a-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="5410a-141">-ODataQuery</span></span>
<span data-ttu-id="5410a-142">Gibt einen Stilfilter des Open Data Protocol (OData) an.</span><span class="sxs-lookup"><span data-stu-id="5410a-142">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="5410a-143">Dieses Cmdlet fügt diesen Wert zusätzlich zu allen anderen Filtern an die Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="5410a-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="5410a-144">-Planen</span><span class="sxs-lookup"><span data-stu-id="5410a-144">-Plan</span></span>
<span data-ttu-id="5410a-145">Gibt Ressourcenplaneigenschaften als Hashtabelle für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="5410a-145">Specifies resource plan properties, as a hash table, for the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5410a-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="5410a-146">-Pre</span></span>
<span data-ttu-id="5410a-147">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5410a-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5410a-148">-Properties</span><span class="sxs-lookup"><span data-stu-id="5410a-148">-Properties</span></span>
<span data-ttu-id="5410a-149">Gibt die Ressourceneigenschaften für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="5410a-149">Specifies resource properties for the resource.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5410a-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5410a-150">-ResourceGroupName</span></span>
<span data-ttu-id="5410a-151">Gibt den Namen der Ressourcengruppe an, in der dieses Cmdlet die Ressource ändert.</span><span class="sxs-lookup"><span data-stu-id="5410a-151">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5410a-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5410a-152">-ResourceId</span></span>
<span data-ttu-id="5410a-153">Gibt die vollqualifizierte Ressourcen-ID einschließlich des Abonnements an, wie im folgenden Beispiel: `/subscriptions/` Abonnement-ID.`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="5410a-153">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5410a-154">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="5410a-154">-ResourceName</span></span>
<span data-ttu-id="5410a-155">Gibt den Namen der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="5410a-155">Specifies the name of the resource.</span></span>
<span data-ttu-id="5410a-156">Um beispielsweise eine Datenbank anzugeben, verwenden Sie das folgende Format: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="5410a-156">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5410a-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="5410a-157">-ResourceType</span></span>
<span data-ttu-id="5410a-158">Gibt den Typ der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="5410a-158">Specifies the type of the resource.</span></span>
<span data-ttu-id="5410a-159">Für eine Datenbank lautet der Ressourcentyp beispielsweise wie folgt: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="5410a-159">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5410a-160">-SKU</span><span class="sxs-lookup"><span data-stu-id="5410a-160">-Sku</span></span>
<span data-ttu-id="5410a-161">Gibt das #A0 der Ressource als Hashtabelle an.</span><span class="sxs-lookup"><span data-stu-id="5410a-161">Specifies the SKU object of the resource as a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5410a-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="5410a-162">-Tag</span></span>
<span data-ttu-id="5410a-163">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="5410a-163">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5410a-164">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="5410a-164">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5410a-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="5410a-165">-TenantLevel</span></span>
<span data-ttu-id="5410a-166">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="5410a-166">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5410a-167">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="5410a-167">-UsePatchSemantics</span></span>
<span data-ttu-id="5410a-168">Gibt an, dass für dieses Cmdlet ein HTTP PATCH zum Aktualisieren des Objekts anstelle einer HTTP PUT verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5410a-168">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="5410a-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5410a-169">-Confirm</span></span>
<span data-ttu-id="5410a-170">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5410a-170">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5410a-171">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5410a-171">-WhatIf</span></span>
<span data-ttu-id="5410a-172">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5410a-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5410a-173">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5410a-173">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5410a-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5410a-174">CommonParameters</span></span>
<span data-ttu-id="5410a-175">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5410a-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5410a-176">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5410a-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5410a-177">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5410a-177">INPUTS</span></span>

### <span data-ttu-id="5410a-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span><span class="sxs-lookup"><span data-stu-id="5410a-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

### <span data-ttu-id="5410a-179">System.String</span><span class="sxs-lookup"><span data-stu-id="5410a-179">System.String</span></span>

### <span data-ttu-id="5410a-180">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="5410a-180">System.Management.Automation.PSObject</span></span>

### <span data-ttu-id="5410a-181">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5410a-181">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5410a-182">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5410a-182">OUTPUTS</span></span>

### <span data-ttu-id="5410a-183">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="5410a-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="5410a-184">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5410a-184">NOTES</span></span>

## <span data-ttu-id="5410a-185">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5410a-185">RELATED LINKS</span></span>


[<span data-ttu-id="5410a-186">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="5410a-186">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="5410a-187">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="5410a-187">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="5410a-188">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="5410a-188">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="5410a-189">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="5410a-189">Remove-AzResource</span></span>](./Remove-AzResource.md)
