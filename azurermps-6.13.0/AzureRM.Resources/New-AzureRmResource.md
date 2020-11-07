---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
ms.openlocfilehash: 57e4bd86ad3f5205749579e190960ea4f8e70588
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662299"
---
# <span data-ttu-id="c8602-101">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c8602-101">New-AzureRmResource</span></span>

## <span data-ttu-id="c8602-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c8602-102">SYNOPSIS</span></span>
<span data-ttu-id="c8602-103">Erstellt eine Ressource.</span><span class="sxs-lookup"><span data-stu-id="c8602-103">Creates a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8602-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8602-104">SYNTAX</span></span>

### <span data-ttu-id="c8602-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="c8602-105">ByResourceId (Default)</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8602-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="c8602-106">BySubscriptionLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8602-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="c8602-107">ByTenantLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c8602-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8602-108">DESCRIPTION</span></span>
<span data-ttu-id="c8602-109">Das Cmdlet **New-AzureRmResource** erstellt eine Azure-Ressource, beispielsweise eine Website, einen Azure SQL-Datenbankserver oder eine Azure SQL-Datenbank, in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c8602-109">The **New-AzureRmResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="c8602-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c8602-110">EXAMPLES</span></span>

### <span data-ttu-id="c8602-111">Beispiel 1: Erstellen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="c8602-111">Example 1: Create a resource</span></span>
```
PS> New-AzureRmResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="c8602-112">Mit diesem Befehl wird eine Ressource erstellt, bei der es sich um eine Website in ResourceGroup11 handelt.</span><span class="sxs-lookup"><span data-stu-id="c8602-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="c8602-113">Beispiel 2: Erstellen einer Ressource mithilfe von splatting</span><span class="sxs-lookup"><span data-stu-id="c8602-113">Example 2: Create a resource using splatting</span></span>
```
PS> $prop = @{
    Location          = "West US" 
    Properties        = @{test = "test"} 
    ResourceName      = "TestSite06" 
    ResourceType      = "microsoft.web/sites" 
    ResourceGroupName = "ResourceGroup11" 
    Force             = $true
}

PS> New-AzureRmResource @prop
```

<span data-ttu-id="c8602-114">Mit diesem Befehl wird eine Ressource erstellt, bei der es sich um eine Website in ResourceGroup11 handelt.</span><span class="sxs-lookup"><span data-stu-id="c8602-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="c8602-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8602-115">PARAMETERS</span></span>

### <span data-ttu-id="c8602-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c8602-116">-ApiVersion</span></span>
<span data-ttu-id="c8602-117">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="c8602-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="c8602-118">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="c8602-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c8602-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8602-119">-AsJob</span></span>
<span data-ttu-id="c8602-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c8602-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8602-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8602-121">-DefaultProfile</span></span>
<span data-ttu-id="c8602-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c8602-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8602-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="c8602-123">-ExtensionResourceName</span></span>
<span data-ttu-id="c8602-124">Gibt den Namen einer Erweiterungs Ressource für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="c8602-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="c8602-125">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: Servername- `/` Datenbankname</span><span class="sxs-lookup"><span data-stu-id="c8602-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="c8602-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="c8602-126">-ExtensionResourceType</span></span>
<span data-ttu-id="c8602-127">Gibt den Ressourcentyp für eine Erweiterungs Ressource an.</span><span class="sxs-lookup"><span data-stu-id="c8602-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="c8602-128">Wenn es sich bei der Erweiterungs Ressource beispielsweise um eine Datenbank handelt, geben Sie den folgenden Typ an: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="c8602-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="c8602-129">-Force</span><span class="sxs-lookup"><span data-stu-id="c8602-129">-Force</span></span>
<span data-ttu-id="c8602-130">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="c8602-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c8602-131">-Isfullobject</span><span class="sxs-lookup"><span data-stu-id="c8602-131">-IsFullObject</span></span>
<span data-ttu-id="c8602-132">Gibt an, dass das Objekt, das der *Properties* -Parameter angibt, das vollständige Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="c8602-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="c8602-133">-Art</span><span class="sxs-lookup"><span data-stu-id="c8602-133">-Kind</span></span>
<span data-ttu-id="c8602-134">Gibt die Art der Ressource für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="c8602-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="c8602-135">-Standort</span><span class="sxs-lookup"><span data-stu-id="c8602-135">-Location</span></span>
<span data-ttu-id="c8602-136">Gibt den Speicherort der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="c8602-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="c8602-137">Geben Sie den Speicherort des Datencenters an, beispielsweise Zentralamerika oder Südostasien.</span><span class="sxs-lookup"><span data-stu-id="c8602-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="c8602-138">Sie können eine Ressource an einem beliebigen Speicherort platzieren, der Ressourcen dieses Typs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c8602-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="c8602-139">Ressourcengruppen können Ressourcen aus unterschiedlichen Speicherorten enthalten.</span><span class="sxs-lookup"><span data-stu-id="c8602-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="c8602-140">Verwenden Sie das Get-AzureLocation-Cmdlet, um zu ermitteln, welche Speicherorte die einzelnen Ressourcentypen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c8602-140">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

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

### <span data-ttu-id="c8602-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="c8602-141">-ODataQuery</span></span>
<span data-ttu-id="c8602-142">Gibt einen Open Data Protocol (OData)-stilfilter an.</span><span class="sxs-lookup"><span data-stu-id="c8602-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="c8602-143">Dieses Cmdlet fügt zusätzlich zu anderen Filtern diesen Wert an die Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="c8602-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="c8602-144">-Plan</span><span class="sxs-lookup"><span data-stu-id="c8602-144">-Plan</span></span>
<span data-ttu-id="c8602-145">Eine Hashtabelle, die Ressourcenplan Eigenschaften darstellt.</span><span class="sxs-lookup"><span data-stu-id="c8602-145">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="c8602-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="c8602-146">-Pre</span></span>
<span data-ttu-id="c8602-147">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c8602-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c8602-148">-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c8602-148">-Properties</span></span>
<span data-ttu-id="c8602-149">Gibt Ressourceneigenschaften für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="c8602-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="c8602-150">Verwenden Sie diesen Parameter, um die Werte von Eigenschaften anzugeben, die für einen Ressourcentyp spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="c8602-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="c8602-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8602-151">-ResourceGroupName</span></span>
<span data-ttu-id="c8602-152">Gibt den Namen der Ressourcengruppe an, in der dieses Cmdlet die Ressource erstellt.</span><span class="sxs-lookup"><span data-stu-id="c8602-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="c8602-153">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c8602-153">-ResourceId</span></span>
<span data-ttu-id="c8602-154">Gibt die vollqualifizierte Ressourcen-ID an, einschließlich des Abonnements, wie im folgenden Beispiel: `/subscriptions/` Abonnement-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="c8602-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="c8602-155">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c8602-155">-ResourceName</span></span>
<span data-ttu-id="c8602-156">Gibt den Namen der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="c8602-156">Specifies the name of the resource.</span></span> <span data-ttu-id="c8602-157">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="c8602-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="c8602-158">-</span><span class="sxs-lookup"><span data-stu-id="c8602-158">-ResourceType</span></span>
<span data-ttu-id="c8602-159">Gibt den Typ der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="c8602-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="c8602-160">Bei einer Datenbank lautet der Ressourcentyp beispielsweise wie folgt: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="c8602-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="c8602-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="c8602-161">-Sku</span></span>
<span data-ttu-id="c8602-162">Eine Hashtabelle, die SKU-Eigenschaften darstellt.</span><span class="sxs-lookup"><span data-stu-id="c8602-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="c8602-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="c8602-163">-Tag</span></span>
<span data-ttu-id="c8602-164">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="c8602-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c8602-165">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="c8602-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c8602-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="c8602-166">-TenantLevel</span></span>
<span data-ttu-id="c8602-167">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="c8602-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="c8602-168">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c8602-168">-Confirm</span></span>
<span data-ttu-id="c8602-169">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c8602-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8602-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8602-170">-WhatIf</span></span>
<span data-ttu-id="c8602-171">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8602-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8602-172">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8602-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8602-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8602-173">CommonParameters</span></span>
<span data-ttu-id="c8602-174">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8602-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8602-175">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8602-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8602-176">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c8602-176">INPUTS</span></span>

### <span data-ttu-id="c8602-177">Keine</span><span class="sxs-lookup"><span data-stu-id="c8602-177">None</span></span>

## <span data-ttu-id="c8602-178">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c8602-178">OUTPUTS</span></span>

### <span data-ttu-id="c8602-179">Microsoft. Azure. Commands. ResourceManagement. Models. PSResource</span><span class="sxs-lookup"><span data-stu-id="c8602-179">Microsoft.Azure.Commands.ResourceManagement.Models.PSResource</span></span>

## <span data-ttu-id="c8602-180">Notizen</span><span class="sxs-lookup"><span data-stu-id="c8602-180">NOTES</span></span>

## <span data-ttu-id="c8602-181">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c8602-181">RELATED LINKS</span></span>

[<span data-ttu-id="c8602-182">Finden-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c8602-182">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="c8602-183">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c8602-183">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="c8602-184">Verschieben-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c8602-184">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="c8602-185">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c8602-185">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="c8602-186">Satz-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c8602-186">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
