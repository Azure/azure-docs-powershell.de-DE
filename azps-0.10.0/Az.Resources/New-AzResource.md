---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResource.md
ms.openlocfilehash: 7ae512f7992392bf12b17775a505313621ec3096
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007583"
---
# <span data-ttu-id="bb248-101">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="bb248-101">New-AzResource</span></span>

## <span data-ttu-id="bb248-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bb248-102">SYNOPSIS</span></span>
<span data-ttu-id="bb248-103">Erstellt eine Ressource.</span><span class="sxs-lookup"><span data-stu-id="bb248-103">Creates a resource.</span></span>

## <span data-ttu-id="bb248-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb248-104">SYNTAX</span></span>

### <span data-ttu-id="bb248-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="bb248-105">ByResourceId (Default)</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb248-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="bb248-106">BySubscriptionLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb248-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="bb248-107">ByTenantLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb248-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb248-108">DESCRIPTION</span></span>
<span data-ttu-id="bb248-109">Das Cmdlet **New-AzResource** erstellt eine Azure-Ressource, beispielsweise eine Website, einen Azure SQL-Datenbankserver oder eine Azure SQL-Datenbank, in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bb248-109">The **New-AzResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="bb248-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bb248-110">EXAMPLES</span></span>

### <span data-ttu-id="bb248-111">Beispiel 1: Erstellen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="bb248-111">Example 1: Create a resource</span></span>
```
PS> New-AzResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="bb248-112">Mit diesem Befehl wird eine Ressource erstellt, bei der es sich um eine Website in ResourceGroup11 handelt.</span><span class="sxs-lookup"><span data-stu-id="bb248-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="bb248-113">Beispiel 2: Erstellen einer Ressource mithilfe von splatting</span><span class="sxs-lookup"><span data-stu-id="bb248-113">Example 2: Create a resource using splatting</span></span>
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

<span data-ttu-id="bb248-114">Mit diesem Befehl wird eine Ressource erstellt, bei der es sich um eine Website in ResourceGroup11 handelt.</span><span class="sxs-lookup"><span data-stu-id="bb248-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="bb248-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb248-115">PARAMETERS</span></span>

### <span data-ttu-id="bb248-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bb248-116">-ApiVersion</span></span>
<span data-ttu-id="bb248-117">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="bb248-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="bb248-118">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="bb248-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="bb248-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb248-119">-AsJob</span></span>
<span data-ttu-id="bb248-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="bb248-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb248-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb248-121">-DefaultProfile</span></span>
<span data-ttu-id="bb248-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="bb248-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb248-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="bb248-123">-ExtensionResourceName</span></span>
<span data-ttu-id="bb248-124">Gibt den Namen einer Erweiterungs Ressource für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="bb248-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="bb248-125">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: Servername- `/` Datenbankname</span><span class="sxs-lookup"><span data-stu-id="bb248-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="bb248-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="bb248-126">-ExtensionResourceType</span></span>
<span data-ttu-id="bb248-127">Gibt den Ressourcentyp für eine Erweiterungs Ressource an.</span><span class="sxs-lookup"><span data-stu-id="bb248-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="bb248-128">Wenn es sich bei der Erweiterungs Ressource beispielsweise um eine Datenbank handelt, geben Sie den folgenden Typ an: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="bb248-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="bb248-129">-Force</span><span class="sxs-lookup"><span data-stu-id="bb248-129">-Force</span></span>
<span data-ttu-id="bb248-130">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="bb248-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bb248-131">-Isfullobject</span><span class="sxs-lookup"><span data-stu-id="bb248-131">-IsFullObject</span></span>
<span data-ttu-id="bb248-132">Gibt an, dass das Objekt, das der *Properties* -Parameter angibt, das vollständige Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="bb248-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="bb248-133">-Art</span><span class="sxs-lookup"><span data-stu-id="bb248-133">-Kind</span></span>
<span data-ttu-id="bb248-134">Gibt die Art der Ressource für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="bb248-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="bb248-135">-Standort</span><span class="sxs-lookup"><span data-stu-id="bb248-135">-Location</span></span>
<span data-ttu-id="bb248-136">Gibt den Speicherort der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="bb248-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="bb248-137">Geben Sie den Speicherort des Datencenters an, beispielsweise Zentralamerika oder Südostasien.</span><span class="sxs-lookup"><span data-stu-id="bb248-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="bb248-138">Sie können eine Ressource an einem beliebigen Speicherort platzieren, der Ressourcen dieses Typs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bb248-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="bb248-139">Ressourcengruppen können Ressourcen aus unterschiedlichen Speicherorten enthalten.</span><span class="sxs-lookup"><span data-stu-id="bb248-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="bb248-140">Verwenden Sie das Get-AzureLocation-Cmdlet, um zu ermitteln, welche Speicherorte die einzelnen Ressourcentypen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="bb248-140">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

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

### <span data-ttu-id="bb248-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="bb248-141">-ODataQuery</span></span>
<span data-ttu-id="bb248-142">Gibt einen Open Data Protocol (OData)-stilfilter an.</span><span class="sxs-lookup"><span data-stu-id="bb248-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="bb248-143">Dieses Cmdlet fügt zusätzlich zu anderen Filtern diesen Wert an die Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="bb248-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="bb248-144">-Plan</span><span class="sxs-lookup"><span data-stu-id="bb248-144">-Plan</span></span>
<span data-ttu-id="bb248-145">Eine Hashtabelle, die Ressourcenplan Eigenschaften darstellt.</span><span class="sxs-lookup"><span data-stu-id="bb248-145">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="bb248-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="bb248-146">-Pre</span></span>
<span data-ttu-id="bb248-147">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="bb248-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="bb248-148">-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bb248-148">-Properties</span></span>
<span data-ttu-id="bb248-149">Gibt Ressourceneigenschaften für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="bb248-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="bb248-150">Verwenden Sie diesen Parameter, um die Werte von Eigenschaften anzugeben, die für einen Ressourcentyp spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="bb248-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="bb248-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb248-151">-ResourceGroupName</span></span>
<span data-ttu-id="bb248-152">Gibt den Namen der Ressourcengruppe an, in der dieses Cmdlet die Ressource erstellt.</span><span class="sxs-lookup"><span data-stu-id="bb248-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="bb248-153">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="bb248-153">-ResourceId</span></span>
<span data-ttu-id="bb248-154">Gibt die vollqualifizierte Ressourcen-ID an, einschließlich des Abonnements, wie im folgenden Beispiel: `/subscriptions/` Abonnement-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="bb248-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="bb248-155">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="bb248-155">-ResourceName</span></span>
<span data-ttu-id="bb248-156">Gibt den Namen der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="bb248-156">Specifies the name of the resource.</span></span> <span data-ttu-id="bb248-157">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="bb248-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="bb248-158">-</span><span class="sxs-lookup"><span data-stu-id="bb248-158">-ResourceType</span></span>
<span data-ttu-id="bb248-159">Gibt den Typ der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="bb248-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="bb248-160">Bei einer Datenbank lautet der Ressourcentyp beispielsweise wie folgt: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="bb248-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="bb248-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="bb248-161">-Sku</span></span>
<span data-ttu-id="bb248-162">Eine Hashtabelle, die SKU-Eigenschaften darstellt.</span><span class="sxs-lookup"><span data-stu-id="bb248-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="bb248-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="bb248-163">-Tag</span></span>
<span data-ttu-id="bb248-164">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="bb248-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bb248-165">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="bb248-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="bb248-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="bb248-166">-TenantLevel</span></span>
<span data-ttu-id="bb248-167">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="bb248-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="bb248-168">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bb248-168">-Confirm</span></span>
<span data-ttu-id="bb248-169">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bb248-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb248-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb248-170">-WhatIf</span></span>
<span data-ttu-id="bb248-171">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bb248-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb248-172">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bb248-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb248-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb248-173">CommonParameters</span></span>
<span data-ttu-id="bb248-174">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb248-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb248-175">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb248-175">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb248-176">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bb248-176">INPUTS</span></span>

### <span data-ttu-id="bb248-177">Keine</span><span class="sxs-lookup"><span data-stu-id="bb248-177">None</span></span>

## <span data-ttu-id="bb248-178">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bb248-178">OUTPUTS</span></span>

### <span data-ttu-id="bb248-179">Microsoft. Azure. Commands. ResourceManagement. Models. PSResource</span><span class="sxs-lookup"><span data-stu-id="bb248-179">Microsoft.Azure.Commands.ResourceManagement.Models.PSResource</span></span>

## <span data-ttu-id="bb248-180">Notizen</span><span class="sxs-lookup"><span data-stu-id="bb248-180">NOTES</span></span>

## <span data-ttu-id="bb248-181">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bb248-181">RELATED LINKS</span></span>

[<span data-ttu-id="bb248-182">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="bb248-182">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="bb248-183">Verschieben-AzResource</span><span class="sxs-lookup"><span data-stu-id="bb248-183">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="bb248-184">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="bb248-184">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="bb248-185">Satz-AzResource</span><span class="sxs-lookup"><span data-stu-id="bb248-185">Set-AzResource</span></span>](./Set-AzResource.md)
