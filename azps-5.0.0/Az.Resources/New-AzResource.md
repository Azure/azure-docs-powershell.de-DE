---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
ms.openlocfilehash: 37561ecc57f5b729a33b2011c26a297bcb2bf52b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300172"
---
# <span data-ttu-id="a76f0-101">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="a76f0-101">New-AzResource</span></span>

## <span data-ttu-id="a76f0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a76f0-102">SYNOPSIS</span></span>
<span data-ttu-id="a76f0-103">Erstellt eine Ressource.</span><span class="sxs-lookup"><span data-stu-id="a76f0-103">Creates a resource.</span></span>

## <span data-ttu-id="a76f0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a76f0-104">SYNTAX</span></span>

### <span data-ttu-id="a76f0-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="a76f0-105">ByResourceId (Default)</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a76f0-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="a76f0-106">BySubscriptionLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a76f0-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="a76f0-107">ByTenantLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a76f0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a76f0-108">DESCRIPTION</span></span>
<span data-ttu-id="a76f0-109">Das Cmdlet **New-AzResource** erstellt eine Azure-Ressource, beispielsweise eine Website, einen Azure SQL-Datenbankserver oder eine Azure SQL-Datenbank, in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a76f0-109">The **New-AzResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="a76f0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a76f0-110">EXAMPLES</span></span>

### <span data-ttu-id="a76f0-111">Beispiel 1: Erstellen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="a76f0-111">Example 1: Create a resource</span></span>
```
PS> New-AzResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="a76f0-112">Mit diesem Befehl wird eine Ressource erstellt, bei der es sich um eine Website in ResourceGroup11 handelt.</span><span class="sxs-lookup"><span data-stu-id="a76f0-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="a76f0-113">Beispiel 2: Erstellen einer Ressource mithilfe von splatting</span><span class="sxs-lookup"><span data-stu-id="a76f0-113">Example 2: Create a resource using splatting</span></span>
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

<span data-ttu-id="a76f0-114">Mit diesem Befehl wird eine Ressource erstellt, bei der es sich um eine Website in ResourceGroup11 handelt.</span><span class="sxs-lookup"><span data-stu-id="a76f0-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="a76f0-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a76f0-115">PARAMETERS</span></span>

### <span data-ttu-id="a76f0-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a76f0-116">-ApiVersion</span></span>
<span data-ttu-id="a76f0-117">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="a76f0-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="a76f0-118">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="a76f0-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a76f0-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a76f0-119">-AsJob</span></span>
<span data-ttu-id="a76f0-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a76f0-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a76f0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a76f0-121">-DefaultProfile</span></span>
<span data-ttu-id="a76f0-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a76f0-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a76f0-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="a76f0-123">-ExtensionResourceName</span></span>
<span data-ttu-id="a76f0-124">Gibt den Namen einer Erweiterungs Ressource für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="a76f0-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="a76f0-125">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: Servername- `/` Datenbankname</span><span class="sxs-lookup"><span data-stu-id="a76f0-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="a76f0-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="a76f0-126">-ExtensionResourceType</span></span>
<span data-ttu-id="a76f0-127">Gibt den Ressourcentyp für eine Erweiterungs Ressource an.</span><span class="sxs-lookup"><span data-stu-id="a76f0-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="a76f0-128">Wenn es sich bei der Erweiterungs Ressource beispielsweise um eine Datenbank handelt, geben Sie den folgenden Typ an: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="a76f0-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="a76f0-129">-Force</span><span class="sxs-lookup"><span data-stu-id="a76f0-129">-Force</span></span>
<span data-ttu-id="a76f0-130">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="a76f0-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a76f0-131">-Isfullobject</span><span class="sxs-lookup"><span data-stu-id="a76f0-131">-IsFullObject</span></span>
<span data-ttu-id="a76f0-132">Gibt an, dass das Objekt, das der *Properties* -Parameter angibt, das vollständige Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="a76f0-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="a76f0-133">-Art</span><span class="sxs-lookup"><span data-stu-id="a76f0-133">-Kind</span></span>
<span data-ttu-id="a76f0-134">Gibt die Art der Ressource für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="a76f0-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="a76f0-135">-Standort</span><span class="sxs-lookup"><span data-stu-id="a76f0-135">-Location</span></span>
<span data-ttu-id="a76f0-136">Gibt den Speicherort der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="a76f0-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="a76f0-137">Geben Sie den Speicherort des Datencenters an, beispielsweise Zentralamerika oder Südostasien.</span><span class="sxs-lookup"><span data-stu-id="a76f0-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="a76f0-138">Sie können eine Ressource an einem beliebigen Speicherort platzieren, der Ressourcen dieses Typs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a76f0-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="a76f0-139">Ressourcengruppen können Ressourcen aus unterschiedlichen Speicherorten enthalten.</span><span class="sxs-lookup"><span data-stu-id="a76f0-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="a76f0-140">Verwenden Sie das Get-AzLocation-Cmdlet, um zu ermitteln, welche Speicherorte die einzelnen Ressourcentypen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a76f0-140">To determine which locations support each resource type, use the Get-AzLocation cmdlet.</span></span>

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

### <span data-ttu-id="a76f0-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="a76f0-141">-ODataQuery</span></span>
<span data-ttu-id="a76f0-142">Gibt einen Open Data Protocol (OData)-stilfilter an.</span><span class="sxs-lookup"><span data-stu-id="a76f0-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="a76f0-143">Dieses Cmdlet fügt zusätzlich zu anderen Filtern diesen Wert an die Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="a76f0-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="a76f0-144">-Plan</span><span class="sxs-lookup"><span data-stu-id="a76f0-144">-Plan</span></span>
<span data-ttu-id="a76f0-145">Eine Hashtabelle, die Ressourcenplan Eigenschaften darstellt.</span><span class="sxs-lookup"><span data-stu-id="a76f0-145">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="a76f0-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="a76f0-146">-Pre</span></span>
<span data-ttu-id="a76f0-147">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="a76f0-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a76f0-148">-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a76f0-148">-Properties</span></span>
<span data-ttu-id="a76f0-149">Gibt Ressourceneigenschaften für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="a76f0-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="a76f0-150">Verwenden Sie diesen Parameter, um die Werte von Eigenschaften anzugeben, die für einen Ressourcentyp spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="a76f0-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="a76f0-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a76f0-151">-ResourceGroupName</span></span>
<span data-ttu-id="a76f0-152">Gibt den Namen der Ressourcengruppe an, in der dieses Cmdlet die Ressource erstellt.</span><span class="sxs-lookup"><span data-stu-id="a76f0-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="a76f0-153">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a76f0-153">-ResourceId</span></span>
<span data-ttu-id="a76f0-154">Gibt die vollqualifizierte Ressourcen-ID an, einschließlich des Abonnements, wie im folgenden Beispiel: `/subscriptions/` Abonnement-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="a76f0-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="a76f0-155">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a76f0-155">-ResourceName</span></span>
<span data-ttu-id="a76f0-156">Gibt den Namen der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="a76f0-156">Specifies the name of the resource.</span></span> <span data-ttu-id="a76f0-157">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="a76f0-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="a76f0-158">-</span><span class="sxs-lookup"><span data-stu-id="a76f0-158">-ResourceType</span></span>
<span data-ttu-id="a76f0-159">Gibt den Typ der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="a76f0-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="a76f0-160">Bei einer Datenbank lautet der Ressourcentyp beispielsweise wie folgt: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="a76f0-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="a76f0-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="a76f0-161">-Sku</span></span>
<span data-ttu-id="a76f0-162">Eine Hashtabelle, die SKU-Eigenschaften darstellt.</span><span class="sxs-lookup"><span data-stu-id="a76f0-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="a76f0-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="a76f0-163">-Tag</span></span>
<span data-ttu-id="a76f0-164">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="a76f0-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a76f0-165">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="a76f0-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a76f0-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="a76f0-166">-TenantLevel</span></span>
<span data-ttu-id="a76f0-167">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="a76f0-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="a76f0-168">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a76f0-168">-Confirm</span></span>
<span data-ttu-id="a76f0-169">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a76f0-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a76f0-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a76f0-170">-WhatIf</span></span>
<span data-ttu-id="a76f0-171">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a76f0-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a76f0-172">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a76f0-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a76f0-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a76f0-173">CommonParameters</span></span>
<span data-ttu-id="a76f0-174">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a76f0-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a76f0-175">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a76f0-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a76f0-176">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a76f0-176">INPUTS</span></span>

### <span data-ttu-id="a76f0-177">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a76f0-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a76f0-178">System. String</span><span class="sxs-lookup"><span data-stu-id="a76f0-178">System.String</span></span>

## <span data-ttu-id="a76f0-179">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a76f0-179">OUTPUTS</span></span>

### <span data-ttu-id="a76f0-180">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a76f0-180">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a76f0-181">Notizen</span><span class="sxs-lookup"><span data-stu-id="a76f0-181">NOTES</span></span>

## <span data-ttu-id="a76f0-182">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a76f0-182">RELATED LINKS</span></span>

[<span data-ttu-id="a76f0-183">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="a76f0-183">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="a76f0-184">Verschieben-AzResource</span><span class="sxs-lookup"><span data-stu-id="a76f0-184">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="a76f0-185">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="a76f0-185">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="a76f0-186">Satz-AzResource</span><span class="sxs-lookup"><span data-stu-id="a76f0-186">Set-AzResource</span></span>](./Set-AzResource.md)
