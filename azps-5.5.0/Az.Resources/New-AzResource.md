---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
ms.openlocfilehash: 37561ecc57f5b729a33b2011c26a297bcb2bf52b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159969"
---
# <span data-ttu-id="aa0a6-101">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="aa0a6-101">New-AzResource</span></span>

## <span data-ttu-id="aa0a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa0a6-102">SYNOPSIS</span></span>
<span data-ttu-id="aa0a6-103">Erstellt eine Ressource.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-103">Creates a resource.</span></span>

## <span data-ttu-id="aa0a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa0a6-104">SYNTAX</span></span>

### <span data-ttu-id="aa0a6-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="aa0a6-105">ByResourceId (Default)</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa0a6-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="aa0a6-106">BySubscriptionLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa0a6-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="aa0a6-107">ByTenantLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa0a6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aa0a6-108">DESCRIPTION</span></span>
<span data-ttu-id="aa0a6-109">Das **Cmdlet "New-AzResource"** erstellt eine Azure-Ressource, z. B. eine Website, einen Azure SQL-Datenbankserver oder eine Azure SQL-Datenbank, in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-109">The **New-AzResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="aa0a6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aa0a6-110">EXAMPLES</span></span>

### <span data-ttu-id="aa0a6-111">Beispiel 1: Erstellen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="aa0a6-111">Example 1: Create a resource</span></span>
```
PS> New-AzResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="aa0a6-112">Mit diesem Befehl wird eine Ressource erstellt, bei der es sich um eine Website in "ResourceGroup11" handelt.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="aa0a6-113">Beispiel 2: Erstellen einer Ressource mithilfe der Plattform</span><span class="sxs-lookup"><span data-stu-id="aa0a6-113">Example 2: Create a resource using splatting</span></span>
```
PS> $prop = @{
    Location          = "West US"
    Properties        = @{test = "test"}
    ResourceName      = "TestSite06"
    ResourceType      = "microsoft.web/sites"
    ResourceGroupName = "ResourceGroup11"
    Force             = $true
}

PS> New-AzResource @prop
```

<span data-ttu-id="aa0a6-114">Mit diesem Befehl wird eine Ressource erstellt, bei der es sich um eine Website in "ResourceGroup11" handelt.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="aa0a6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa0a6-115">PARAMETERS</span></span>

### <span data-ttu-id="aa0a6-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="aa0a6-116">-ApiVersion</span></span>
<span data-ttu-id="aa0a6-117">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="aa0a6-118">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="aa0a6-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa0a6-119">-AsJob</span></span>
<span data-ttu-id="aa0a6-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="aa0a6-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa0a6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa0a6-121">-DefaultProfile</span></span>
<span data-ttu-id="aa0a6-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="aa0a6-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa0a6-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="aa0a6-123">-ExtensionResourceName</span></span>
<span data-ttu-id="aa0a6-124">Gibt den Namen einer Erweiterungsressource für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="aa0a6-125">Um beispielsweise eine Datenbank anzugeben, verwenden Sie das folgende Format: Name der `/` Serverdatenbank</span><span class="sxs-lookup"><span data-stu-id="aa0a6-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="aa0a6-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="aa0a6-126">-ExtensionResourceType</span></span>
<span data-ttu-id="aa0a6-127">Gibt den Ressourcentyp für eine Erweiterungsressource an.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="aa0a6-128">Wenn es sich bei der Erweiterungsressource beispielsweise um eine Datenbank handelt, geben Sie den folgenden Typ an: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="aa0a6-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="aa0a6-129">-Force</span><span class="sxs-lookup"><span data-stu-id="aa0a6-129">-Force</span></span>
<span data-ttu-id="aa0a6-130">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aa0a6-131">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="aa0a6-131">-IsFullObject</span></span>
<span data-ttu-id="aa0a6-132">Gibt an, dass das vom Parameter *"Properties"* angegebene Objekt das vollständige Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="aa0a6-133">-Kind</span><span class="sxs-lookup"><span data-stu-id="aa0a6-133">-Kind</span></span>
<span data-ttu-id="aa0a6-134">Gibt die Ressourcentyp für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="aa0a6-135">-Location</span><span class="sxs-lookup"><span data-stu-id="aa0a6-135">-Location</span></span>
<span data-ttu-id="aa0a6-136">Gibt den Speicherort der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="aa0a6-137">Geben Sie den Standort des Rechenzentrums an, z. B. "Zentral-USA" oder "Südostasien".</span><span class="sxs-lookup"><span data-stu-id="aa0a6-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="aa0a6-138">Sie können eine Ressource an einem beliebigen Ort platzieren, der Ressourcen dieses Typs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="aa0a6-139">Ressourcengruppen können Ressourcen von verschiedenen Standorten enthalten.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="aa0a6-140">Um festzustellen, welche Speicherorte die einzelnen Ressourcentypen unterstützen, verwenden Sie Get-AzLocation-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-140">To determine which locations support each resource type, use the Get-AzLocation cmdlet.</span></span>

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

### <span data-ttu-id="aa0a6-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="aa0a6-141">-ODataQuery</span></span>
<span data-ttu-id="aa0a6-142">Gibt einen Stilfilter vom Datentyp "Open Data Protocol" (OData) an.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="aa0a6-143">Dieses Cmdlet fügt diesen Wert zusätzlich zu allen anderen Filtern an die Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="aa0a6-144">-Planen</span><span class="sxs-lookup"><span data-stu-id="aa0a6-144">-Plan</span></span>
<span data-ttu-id="aa0a6-145">Eine Hashtabelle, die Ressourcenplaneigenschaften darstellt.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-145">A hash table that represents resource plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa0a6-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="aa0a6-146">-Pre</span></span>
<span data-ttu-id="aa0a6-147">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="aa0a6-148">-Properties</span><span class="sxs-lookup"><span data-stu-id="aa0a6-148">-Properties</span></span>
<span data-ttu-id="aa0a6-149">Gibt die Ressourceneigenschaften für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="aa0a6-150">Verwenden Sie diesen Parameter, um die Werte von Eigenschaften anzugeben, die für einen Ressourcentyp spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa0a6-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa0a6-151">-ResourceGroupName</span></span>
<span data-ttu-id="aa0a6-152">Gibt den Namen der Ressourcengruppe an, in der dieses Cmdlet die Ressource erstellt.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="aa0a6-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa0a6-153">-ResourceId</span></span>
<span data-ttu-id="aa0a6-154">Gibt die vollqualifizierte Ressourcen-ID einschließlich des Abonnements an, wie im folgenden Beispiel: `/subscriptions/` Abonnement-ID.`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="aa0a6-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="aa0a6-155">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="aa0a6-155">-ResourceName</span></span>
<span data-ttu-id="aa0a6-156">Gibt den Namen der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-156">Specifies the name of the resource.</span></span> <span data-ttu-id="aa0a6-157">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="aa0a6-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="aa0a6-158">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="aa0a6-158">-ResourceType</span></span>
<span data-ttu-id="aa0a6-159">Gibt den Typ der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="aa0a6-160">Für eine Datenbank lautet der Ressourcentyp beispielsweise wie folgt: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="aa0a6-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="aa0a6-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="aa0a6-161">-Sku</span></span>
<span data-ttu-id="aa0a6-162">Eine Hashtabelle, die #A0 darstellt.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="aa0a6-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="aa0a6-163">-Tag</span></span>
<span data-ttu-id="aa0a6-164">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="aa0a6-165">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="aa0a6-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa0a6-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="aa0a6-166">-TenantLevel</span></span>
<span data-ttu-id="aa0a6-167">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="aa0a6-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa0a6-168">-Confirm</span></span>
<span data-ttu-id="aa0a6-169">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa0a6-170">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="aa0a6-170">-WhatIf</span></span>
<span data-ttu-id="aa0a6-171">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa0a6-172">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa0a6-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa0a6-173">CommonParameters</span></span>
<span data-ttu-id="aa0a6-174">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa0a6-175">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa0a6-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa0a6-176">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aa0a6-176">INPUTS</span></span>

### <span data-ttu-id="aa0a6-177">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="aa0a6-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="aa0a6-178">System.String</span><span class="sxs-lookup"><span data-stu-id="aa0a6-178">System.String</span></span>

## <span data-ttu-id="aa0a6-179">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aa0a6-179">OUTPUTS</span></span>

### <span data-ttu-id="aa0a6-180">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="aa0a6-180">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="aa0a6-181">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="aa0a6-181">NOTES</span></span>

## <span data-ttu-id="aa0a6-182">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="aa0a6-182">RELATED LINKS</span></span>

[<span data-ttu-id="aa0a6-183">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="aa0a6-183">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="aa0a6-184">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="aa0a6-184">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="aa0a6-185">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="aa0a6-185">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="aa0a6-186">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="aa0a6-186">Set-AzResource</span></span>](./Set-AzResource.md)
