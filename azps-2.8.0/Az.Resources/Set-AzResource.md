---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
ms.openlocfilehash: a47d9a985adba97659ffac84d054b418daf1bc02
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "93851048"
---
# <span data-ttu-id="59823-101">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="59823-101">Set-AzResource</span></span>

## <span data-ttu-id="59823-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="59823-102">SYNOPSIS</span></span>
<span data-ttu-id="59823-103">Ändert eine Ressource.</span><span class="sxs-lookup"><span data-stu-id="59823-103">Modifies a resource.</span></span>

## <span data-ttu-id="59823-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="59823-104">SYNTAX</span></span>

### <span data-ttu-id="59823-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="59823-105">ByResourceId (Default)</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59823-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="59823-106">ByInputObject</span></span>
```
Set-AzResource -InputObject <PSResource> [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59823-107">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="59823-107">BySubscriptionLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59823-108">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="59823-108">ByTenantLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59823-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59823-109">DESCRIPTION</span></span>
<span data-ttu-id="59823-110">Das Cmdlet " **Satz-AzResource** " ändert eine vorhandene Azure-Ressource.</span><span class="sxs-lookup"><span data-stu-id="59823-110">The **Set-AzResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="59823-111">Geben Sie eine Ressource an, die nach Name und Typ oder nach ID geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="59823-111">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="59823-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59823-112">EXAMPLES</span></span>

### <span data-ttu-id="59823-113">Beispiel 1: Ändern einer Ressource</span><span class="sxs-lookup"><span data-stu-id="59823-113">Example 1: Modify a resource</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceType Microsoft.Web/sites -ResourceGroupName ResourceGroup11 -ResourceName ContosoSite
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzResource -Force
```

<span data-ttu-id="59823-114">Der erste Befehl ruft die Ressource mit dem Namen ContosoSite mithilfe des Get-AzResource-Cmdlets ab und speichert Sie dann in der $Resource-Variablen.</span><span class="sxs-lookup"><span data-stu-id="59823-114">The first command gets the resource named ContosoSite by using the Get-AzResource cmdlet, and then stores it in the $Resource variable.</span></span>
<span data-ttu-id="59823-115">Der zweite Befehl ändert eine Eigenschaft von $Resource.</span><span class="sxs-lookup"><span data-stu-id="59823-115">The second command modifies a property of $Resource.</span></span>
<span data-ttu-id="59823-116">Mit dem letzten Befehl wird die Ressource so aktualisiert, dass Sie $Resource entspricht.</span><span class="sxs-lookup"><span data-stu-id="59823-116">The final command updates the resource to match $Resource.</span></span>

### <span data-ttu-id="59823-117">Beispiel 2: Ändern aller Ressourcen in einer bestimmten Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="59823-117">Example 2: Modify all resources in a given resource group</span></span>
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

<span data-ttu-id="59823-118">Der erste Befehl ruft die Ressourcen in der testrg-Ressourcengruppe ab und speichert Sie dann in der $Resource-Variablen.</span><span class="sxs-lookup"><span data-stu-id="59823-118">The first command gets the resources in the testrg resource group, and then stores them in the $Resource variable.</span></span>

<span data-ttu-id="59823-119">Der zweite Befehl iteriert über jede dieser Ressourcen in der Ressourcengruppe und fügt ihnen ein neues Tag hinzu.</span><span class="sxs-lookup"><span data-stu-id="59823-119">The second command iterates over each of these resources in the resource group and adds a new tag to them.</span></span>

<span data-ttu-id="59823-120">Der endgültige Befehl aktualisiert jede dieser Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="59823-120">The final command updates each of these resources.</span></span>

## <span data-ttu-id="59823-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="59823-121">PARAMETERS</span></span>

### <span data-ttu-id="59823-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="59823-122">-ApiVersion</span></span>
<span data-ttu-id="59823-123">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="59823-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="59823-124">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="59823-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="59823-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59823-125">-AsJob</span></span>
<span data-ttu-id="59823-126">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="59823-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59823-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59823-127">-DefaultProfile</span></span>
<span data-ttu-id="59823-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="59823-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59823-129">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="59823-129">-ExtensionResourceName</span></span>
<span data-ttu-id="59823-130">Gibt den Namen einer Erweiterungs Ressource für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="59823-130">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="59823-131">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: Servername- `/` Datenbankname</span><span class="sxs-lookup"><span data-stu-id="59823-131">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="59823-132">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="59823-132">-ExtensionResourceType</span></span>
<span data-ttu-id="59823-133">Gibt den Ressourcentyp für eine Erweiterungs Ressource an.</span><span class="sxs-lookup"><span data-stu-id="59823-133">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="59823-134">Wenn beispielsweise die Erweiterungs Ressource eine Datenbank ist, geben Sie Folgendes an: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="59823-134">For instance, if the extension resource is a database specify the following: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="59823-135">-Force</span><span class="sxs-lookup"><span data-stu-id="59823-135">-Force</span></span>
<span data-ttu-id="59823-136">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="59823-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="59823-137">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="59823-137">-InputObject</span></span>
<span data-ttu-id="59823-138">Die Objektdarstellung der Ressource, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="59823-138">The object representation of the resource to update.</span></span>

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

### <span data-ttu-id="59823-139">-Art</span><span class="sxs-lookup"><span data-stu-id="59823-139">-Kind</span></span>
<span data-ttu-id="59823-140">Gibt die Art der Ressource für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="59823-140">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="59823-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="59823-141">-ODataQuery</span></span>
<span data-ttu-id="59823-142">Gibt einen Open Data Protocol (OData)-stilfilter an.</span><span class="sxs-lookup"><span data-stu-id="59823-142">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="59823-143">Dieses Cmdlet fügt zusätzlich zu anderen Filtern diesen Wert an die Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="59823-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="59823-144">-Plan</span><span class="sxs-lookup"><span data-stu-id="59823-144">-Plan</span></span>
<span data-ttu-id="59823-145">Gibt Ressourcenplan Eigenschaften als Hashtabelle für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="59823-145">Specifies resource plan properties, as a hash table, for the resource.</span></span>

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

### <span data-ttu-id="59823-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="59823-146">-Pre</span></span>
<span data-ttu-id="59823-147">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="59823-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="59823-148">-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="59823-148">-Properties</span></span>
<span data-ttu-id="59823-149">Gibt Ressourceneigenschaften für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="59823-149">Specifies resource properties for the resource.</span></span>

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

### <span data-ttu-id="59823-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59823-150">-ResourceGroupName</span></span>
<span data-ttu-id="59823-151">Gibt den Namen der Ressourcengruppe an, in der dieses Cmdlet die Ressource ändert.</span><span class="sxs-lookup"><span data-stu-id="59823-151">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="59823-152">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="59823-152">-ResourceId</span></span>
<span data-ttu-id="59823-153">Gibt die vollqualifizierte Ressourcen-ID an, einschließlich des Abonnements, wie im folgenden Beispiel: `/subscriptions/` Abonnement-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="59823-153">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="59823-154">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="59823-154">-ResourceName</span></span>
<span data-ttu-id="59823-155">Gibt den Namen der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="59823-155">Specifies the name of the resource.</span></span>
<span data-ttu-id="59823-156">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="59823-156">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="59823-157">-</span><span class="sxs-lookup"><span data-stu-id="59823-157">-ResourceType</span></span>
<span data-ttu-id="59823-158">Gibt den Typ der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="59823-158">Specifies the type of the resource.</span></span>
<span data-ttu-id="59823-159">Bei einer Datenbank lautet der Ressourcentyp beispielsweise wie folgt: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="59823-159">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="59823-160">-SKU</span><span class="sxs-lookup"><span data-stu-id="59823-160">-Sku</span></span>
<span data-ttu-id="59823-161">Gibt das SKU-Objekt der Ressource als Hashtabelle an.</span><span class="sxs-lookup"><span data-stu-id="59823-161">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="59823-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="59823-162">-Tag</span></span>
<span data-ttu-id="59823-163">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="59823-163">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="59823-164">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="59823-164">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="59823-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="59823-165">-TenantLevel</span></span>
<span data-ttu-id="59823-166">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="59823-166">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="59823-167">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="59823-167">-UsePatchSemantics</span></span>
<span data-ttu-id="59823-168">Gibt an, dass dieses Cmdlet anstelle eines HTTP-PUT einen HTTP-Patch zum Aktualisieren des Objekts verwendet.</span><span class="sxs-lookup"><span data-stu-id="59823-168">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="59823-169">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="59823-169">-Confirm</span></span>
<span data-ttu-id="59823-170">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="59823-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59823-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59823-171">-WhatIf</span></span>
<span data-ttu-id="59823-172">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59823-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59823-173">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="59823-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59823-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59823-174">CommonParameters</span></span>
<span data-ttu-id="59823-175">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59823-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59823-176">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59823-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59823-177">Eingaben</span><span class="sxs-lookup"><span data-stu-id="59823-177">INPUTS</span></span>

### <span data-ttu-id="59823-178">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResource</span><span class="sxs-lookup"><span data-stu-id="59823-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

### <span data-ttu-id="59823-179">System. String</span><span class="sxs-lookup"><span data-stu-id="59823-179">System.String</span></span>

### <span data-ttu-id="59823-180">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="59823-180">System.Management.Automation.PSObject</span></span>

### <span data-ttu-id="59823-181">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="59823-181">System.Collections.Hashtable</span></span>

## <span data-ttu-id="59823-182">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59823-182">OUTPUTS</span></span>

### <span data-ttu-id="59823-183">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="59823-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="59823-184">Notizen</span><span class="sxs-lookup"><span data-stu-id="59823-184">NOTES</span></span>

## <span data-ttu-id="59823-185">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="59823-185">RELATED LINKS</span></span>

[<span data-ttu-id="59823-186">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="59823-186">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="59823-187">Verschieben-AzResource</span><span class="sxs-lookup"><span data-stu-id="59823-187">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="59823-188">Neu – AzResource</span><span class="sxs-lookup"><span data-stu-id="59823-188">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="59823-189">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="59823-189">Remove-AzResource</span></span>](./Remove-AzResource.md)
