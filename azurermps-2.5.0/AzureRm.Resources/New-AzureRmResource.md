---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresource
schema: 2.0.0
ms.openlocfilehash: 820c0fcc328542bd066fce58f13cfde284e5b415
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850252"
---
# <span data-ttu-id="502be-101">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="502be-101">New-AzureRmResource</span></span>

## <span data-ttu-id="502be-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="502be-102">SYNOPSIS</span></span>
<span data-ttu-id="502be-103">Erstellt eine Ressource.</span><span class="sxs-lookup"><span data-stu-id="502be-103">Creates a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="502be-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="502be-104">SYNTAX</span></span>

### <span data-ttu-id="502be-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="502be-105">ByResourceId (Default)</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="502be-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="502be-106">BySubscriptionLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="502be-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="502be-107">ByTenantLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="502be-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="502be-108">DESCRIPTION</span></span>
<span data-ttu-id="502be-109">Das Cmdlet **New-AzureRmResource** erstellt eine Azure-Ressource, beispielsweise eine Website, einen Azure SQL-Datenbankserver oder eine Azure SQL-Datenbank, in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="502be-109">The **New-AzureRmResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="502be-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="502be-110">EXAMPLES</span></span>

### <span data-ttu-id="502be-111">Beispiel 1: Erstellen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="502be-111">Example 1: Create a resource</span></span>
```
PS> New-AzureRmResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="502be-112">Mit diesem Befehl wird eine Ressource erstellt, bei der es sich um eine Website in ResourceGroup11 handelt.</span><span class="sxs-lookup"><span data-stu-id="502be-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="502be-113">Beispiel 2: Erstellen einer Ressource mithilfe von splatting</span><span class="sxs-lookup"><span data-stu-id="502be-113">Example 2: Create a resource using splatting</span></span>
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

<span data-ttu-id="502be-114">Mit diesem Befehl wird eine Ressource erstellt, bei der es sich um eine Website in ResourceGroup11 handelt.</span><span class="sxs-lookup"><span data-stu-id="502be-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="502be-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="502be-115">PARAMETERS</span></span>

### <span data-ttu-id="502be-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="502be-116">-ApiVersion</span></span>
<span data-ttu-id="502be-117">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="502be-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="502be-118">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="502be-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="502be-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="502be-119">-AsJob</span></span>
<span data-ttu-id="502be-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="502be-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="502be-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="502be-121">-DefaultProfile</span></span>
<span data-ttu-id="502be-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="502be-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="502be-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="502be-123">-ExtensionResourceName</span></span>
<span data-ttu-id="502be-124">Gibt den Namen einer Erweiterungs Ressource für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="502be-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="502be-125">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: Servername- `/` Datenbankname</span><span class="sxs-lookup"><span data-stu-id="502be-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="502be-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="502be-126">-ExtensionResourceType</span></span>
<span data-ttu-id="502be-127">Gibt den Ressourcentyp für eine Erweiterungs Ressource an.</span><span class="sxs-lookup"><span data-stu-id="502be-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="502be-128">Wenn es sich bei der Erweiterungs Ressource beispielsweise um eine Datenbank handelt, geben Sie den folgenden Typ an: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="502be-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="502be-129">-Force</span><span class="sxs-lookup"><span data-stu-id="502be-129">-Force</span></span>
<span data-ttu-id="502be-130">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="502be-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="502be-131">-Isfullobject</span><span class="sxs-lookup"><span data-stu-id="502be-131">-IsFullObject</span></span>
<span data-ttu-id="502be-132">Gibt an, dass das Objekt, das der *Properties* -Parameter angibt, das vollständige Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="502be-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="502be-133">-Art</span><span class="sxs-lookup"><span data-stu-id="502be-133">-Kind</span></span>
<span data-ttu-id="502be-134">Gibt die Art der Ressource für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="502be-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="502be-135">-Standort</span><span class="sxs-lookup"><span data-stu-id="502be-135">-Location</span></span>
<span data-ttu-id="502be-136">Gibt den Speicherort der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="502be-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="502be-137">Geben Sie den Speicherort des Datencenters an, beispielsweise Zentralamerika oder Südostasien.</span><span class="sxs-lookup"><span data-stu-id="502be-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="502be-138">Sie können eine Ressource an einem beliebigen Speicherort platzieren, der Ressourcen dieses Typs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="502be-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="502be-139">Ressourcengruppen können Ressourcen aus unterschiedlichen Speicherorten enthalten.</span><span class="sxs-lookup"><span data-stu-id="502be-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="502be-140">Verwenden Sie das Get-AzureLocation-Cmdlet, um zu ermitteln, welche Speicherorte die einzelnen Ressourcentypen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="502be-140">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

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

### <span data-ttu-id="502be-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="502be-141">-ODataQuery</span></span>
<span data-ttu-id="502be-142">Gibt einen Open Data Protocol (OData)-stilfilter an.</span><span class="sxs-lookup"><span data-stu-id="502be-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="502be-143">Dieses Cmdlet fügt zusätzlich zu anderen Filtern diesen Wert an die Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="502be-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="502be-144">-Plan</span><span class="sxs-lookup"><span data-stu-id="502be-144">-Plan</span></span>
<span data-ttu-id="502be-145">Eine Hashtabelle, die Ressourcenplan Eigenschaften darstellt.</span><span class="sxs-lookup"><span data-stu-id="502be-145">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="502be-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="502be-146">-Pre</span></span>
<span data-ttu-id="502be-147">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="502be-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="502be-148">-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="502be-148">-Properties</span></span>
<span data-ttu-id="502be-149">Gibt Ressourceneigenschaften für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="502be-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="502be-150">Verwenden Sie diesen Parameter, um die Werte von Eigenschaften anzugeben, die für einen Ressourcentyp spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="502be-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="502be-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="502be-151">-ResourceGroupName</span></span>
<span data-ttu-id="502be-152">Gibt den Namen der Ressourcengruppe an, in der dieses Cmdlet die Ressource erstellt.</span><span class="sxs-lookup"><span data-stu-id="502be-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="502be-153">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="502be-153">-ResourceId</span></span>
<span data-ttu-id="502be-154">Gibt die vollqualifizierte Ressourcen-ID an, einschließlich des Abonnements, wie im folgenden Beispiel: `/subscriptions/` Abonnement-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="502be-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="502be-155">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="502be-155">-ResourceName</span></span>
<span data-ttu-id="502be-156">Gibt den Namen der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="502be-156">Specifies the name of the resource.</span></span> <span data-ttu-id="502be-157">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="502be-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="502be-158">-</span><span class="sxs-lookup"><span data-stu-id="502be-158">-ResourceType</span></span>
<span data-ttu-id="502be-159">Gibt den Typ der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="502be-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="502be-160">Bei einer Datenbank lautet der Ressourcentyp beispielsweise wie folgt: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="502be-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="502be-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="502be-161">-Sku</span></span>
<span data-ttu-id="502be-162">Eine Hashtabelle, die SKU-Eigenschaften darstellt.</span><span class="sxs-lookup"><span data-stu-id="502be-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="502be-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="502be-163">-Tag</span></span>
<span data-ttu-id="502be-164">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="502be-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="502be-165">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="502be-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="502be-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="502be-166">-TenantLevel</span></span>
<span data-ttu-id="502be-167">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="502be-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="502be-168">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="502be-168">-Confirm</span></span>
<span data-ttu-id="502be-169">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="502be-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="502be-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="502be-170">-WhatIf</span></span>
<span data-ttu-id="502be-171">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="502be-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="502be-172">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="502be-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="502be-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="502be-173">CommonParameters</span></span>
<span data-ttu-id="502be-174">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="502be-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="502be-175">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="502be-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="502be-176">Eingaben</span><span class="sxs-lookup"><span data-stu-id="502be-176">INPUTS</span></span>

### <span data-ttu-id="502be-177">Keine</span><span class="sxs-lookup"><span data-stu-id="502be-177">None</span></span>

## <span data-ttu-id="502be-178">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="502be-178">OUTPUTS</span></span>

### <span data-ttu-id="502be-179">Microsoft. Azure. Commands. ResourceManagement. Models. PSResource</span><span class="sxs-lookup"><span data-stu-id="502be-179">Microsoft.Azure.Commands.ResourceManagement.Models.PSResource</span></span>

## <span data-ttu-id="502be-180">Notizen</span><span class="sxs-lookup"><span data-stu-id="502be-180">NOTES</span></span>

## <span data-ttu-id="502be-181">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="502be-181">RELATED LINKS</span></span>



[<span data-ttu-id="502be-182">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="502be-182">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="502be-183">Verschieben-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="502be-183">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="502be-184">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="502be-184">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="502be-185">Satz-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="502be-185">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
