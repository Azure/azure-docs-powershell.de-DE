---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
ms.openlocfilehash: c7a98f6fba2c690fb296c42f4f6eca902d7678bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480962"
---
# <span data-ttu-id="800c3-101">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="800c3-101">New-AzureRmResource</span></span>

## <span data-ttu-id="800c3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="800c3-102">SYNOPSIS</span></span>
<span data-ttu-id="800c3-103">Erstellt eine Ressource.</span><span class="sxs-lookup"><span data-stu-id="800c3-103">Creates a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="800c3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="800c3-104">SYNTAX</span></span>

### <span data-ttu-id="800c3-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="800c3-105">ByResourceId (Default)</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="800c3-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="800c3-106">BySubscriptionLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="800c3-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="800c3-107">ByTenantLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="800c3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="800c3-108">DESCRIPTION</span></span>
<span data-ttu-id="800c3-109">Das Cmdlet **New-AzureRmResource** erstellt eine Azure-Ressource, beispielsweise eine Website, einen Azure SQL-Datenbankserver oder eine Azure SQL-Datenbank, in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="800c3-109">The **New-AzureRmResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="800c3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="800c3-110">EXAMPLES</span></span>

### <span data-ttu-id="800c3-111">Beispiel 1: Erstellen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="800c3-111">Example 1: Create a resource</span></span>
```
PS> New-AzureRmResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="800c3-112">Mit diesem Befehl wird eine Ressource erstellt, bei der es sich um eine Website in ResourceGroup11 handelt.</span><span class="sxs-lookup"><span data-stu-id="800c3-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="800c3-113">Beispiel 2: Erstellen einer Ressource mithilfe von splatting</span><span class="sxs-lookup"><span data-stu-id="800c3-113">Example 2: Create a resource using splatting</span></span>
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

<span data-ttu-id="800c3-114">Mit diesem Befehl wird eine Ressource erstellt, bei der es sich um eine Website in ResourceGroup11 handelt.</span><span class="sxs-lookup"><span data-stu-id="800c3-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="800c3-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="800c3-115">PARAMETERS</span></span>

### <span data-ttu-id="800c3-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="800c3-116">-ApiVersion</span></span>
<span data-ttu-id="800c3-117">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="800c3-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="800c3-118">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="800c3-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800c3-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="800c3-119">-AsJob</span></span>
<span data-ttu-id="800c3-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="800c3-120">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800c3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="800c3-121">-DefaultProfile</span></span>
<span data-ttu-id="800c3-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="800c3-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800c3-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="800c3-123">-ExtensionResourceName</span></span>
<span data-ttu-id="800c3-124">Gibt den Namen einer Erweiterungs Ressource für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="800c3-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="800c3-125">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="800c3-125">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="800c3-126">Name der Servernamen- `/` Datenbank</span><span class="sxs-lookup"><span data-stu-id="800c3-126">server name`/`database name</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="800c3-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="800c3-127">-ExtensionResourceType</span></span>
<span data-ttu-id="800c3-128">Gibt den Ressourcentyp für eine Erweiterungs Ressource an.</span><span class="sxs-lookup"><span data-stu-id="800c3-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="800c3-129">Wenn es sich bei der Erweiterungs Ressource beispielsweise um eine Datenbank handelt, geben Sie den folgenden Typ an:</span><span class="sxs-lookup"><span data-stu-id="800c3-129">For instance, if the extension resource is a database, specify the following type:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="800c3-130">-Force</span><span class="sxs-lookup"><span data-stu-id="800c3-130">-Force</span></span>
<span data-ttu-id="800c3-131">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="800c3-131">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800c3-132">-Isfullobject</span><span class="sxs-lookup"><span data-stu-id="800c3-132">-IsFullObject</span></span>
<span data-ttu-id="800c3-133">Gibt an, dass das Objekt, das der *Properties* -Parameter angibt, das vollständige Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="800c3-133">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800c3-134">-Art</span><span class="sxs-lookup"><span data-stu-id="800c3-134">-Kind</span></span>
<span data-ttu-id="800c3-135">Gibt die Art der Ressource für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="800c3-135">Specifies the resource kind for the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800c3-136">-Standort</span><span class="sxs-lookup"><span data-stu-id="800c3-136">-Location</span></span>
<span data-ttu-id="800c3-137">Gibt den Speicherort der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="800c3-137">Specifies the location of the resource.</span></span>
<span data-ttu-id="800c3-138">Geben Sie den Speicherort des Datencenters an, beispielsweise Zentralamerika oder Südostasien.</span><span class="sxs-lookup"><span data-stu-id="800c3-138">Specify data center location, such as Central US or Southeast Asia.</span></span>

<span data-ttu-id="800c3-139">Sie können eine Ressource an einem beliebigen Speicherort platzieren, der Ressourcen dieses Typs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="800c3-139">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="800c3-140">Ressourcengruppen können Ressourcen aus unterschiedlichen Speicherorten enthalten.</span><span class="sxs-lookup"><span data-stu-id="800c3-140">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="800c3-141">Verwenden Sie das Get-AzureLocation-Cmdlet, um zu ermitteln, welche Speicherorte die einzelnen Ressourcentypen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="800c3-141">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800c3-142">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="800c3-142">-ODataQuery</span></span>
<span data-ttu-id="800c3-143">Gibt einen Open Data Protocol (OData)-stilfilter an.</span><span class="sxs-lookup"><span data-stu-id="800c3-143">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="800c3-144">Dieses Cmdlet fügt zusätzlich zu anderen Filtern diesen Wert an die Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="800c3-144">This cmdlet appends this value to the request in addition to any other filters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800c3-145">-Plan</span><span class="sxs-lookup"><span data-stu-id="800c3-145">-Plan</span></span>
<span data-ttu-id="800c3-146">Eine Hashtabelle, die Ressourcenplan Eigenschaften darstellt.</span><span class="sxs-lookup"><span data-stu-id="800c3-146">A hash table that represents resource plan properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800c3-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="800c3-147">-Pre</span></span>
<span data-ttu-id="800c3-148">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="800c3-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800c3-149">-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="800c3-149">-Properties</span></span>
<span data-ttu-id="800c3-150">Gibt Ressourceneigenschaften für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="800c3-150">Specifies resource properties for the resource.</span></span> <span data-ttu-id="800c3-151">Verwenden Sie diesen Parameter, um die Werte von Eigenschaften anzugeben, die für einen Ressourcentyp spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="800c3-151">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800c3-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="800c3-152">-ResourceGroupName</span></span>
<span data-ttu-id="800c3-153">Gibt den Namen der Ressourcengruppe an, in der dieses Cmdlet die Ressource erstellt.</span><span class="sxs-lookup"><span data-stu-id="800c3-153">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="800c3-154">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="800c3-154">-ResourceId</span></span>
<span data-ttu-id="800c3-155">Gibt die vollqualifizierte Ressourcen-ID an, einschließlich des Abonnements, wie im folgenden Beispiel:</span><span class="sxs-lookup"><span data-stu-id="800c3-155">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="800c3-156">`/subscriptions/`Abonnement-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="800c3-156">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="800c3-157">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="800c3-157">-ResourceName</span></span>
<span data-ttu-id="800c3-158">Gibt den Namen der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="800c3-158">Specifies the name of the resource.</span></span> <span data-ttu-id="800c3-159">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="800c3-159">For instance, to specify a database, use the following format:</span></span>

`ContosoServer/ContosoDatabase`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="800c3-160">-</span><span class="sxs-lookup"><span data-stu-id="800c3-160">-ResourceType</span></span>
<span data-ttu-id="800c3-161">Gibt den Typ der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="800c3-161">Specifies the type of the resource.</span></span>
<span data-ttu-id="800c3-162">Bei einer Datenbank lautet der Ressourcentyp beispielsweise wie folgt:</span><span class="sxs-lookup"><span data-stu-id="800c3-162">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="800c3-163">-SKU</span><span class="sxs-lookup"><span data-stu-id="800c3-163">-Sku</span></span>
<span data-ttu-id="800c3-164">Eine Hashtabelle, die SKU-Eigenschaften darstellt.</span><span class="sxs-lookup"><span data-stu-id="800c3-164">A hash table that represents sku properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="800c3-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="800c3-165">-Tag</span></span>
<span data-ttu-id="800c3-166">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="800c3-166">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="800c3-167">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="800c3-167">For example:</span></span>

<span data-ttu-id="800c3-168">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="800c3-168">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800c3-169">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="800c3-169">-TenantLevel</span></span>
<span data-ttu-id="800c3-170">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="800c3-170">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800c3-171">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="800c3-171">-Confirm</span></span>
<span data-ttu-id="800c3-172">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="800c3-172">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800c3-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="800c3-173">-WhatIf</span></span>
<span data-ttu-id="800c3-174">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="800c3-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="800c3-175">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="800c3-175">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800c3-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="800c3-176">CommonParameters</span></span>
<span data-ttu-id="800c3-177">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="800c3-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="800c3-178">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="800c3-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="800c3-179">Eingaben</span><span class="sxs-lookup"><span data-stu-id="800c3-179">INPUTS</span></span>

### <span data-ttu-id="800c3-180">Keine</span><span class="sxs-lookup"><span data-stu-id="800c3-180">None</span></span>
<span data-ttu-id="800c3-181">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="800c3-181">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="800c3-182">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="800c3-182">OUTPUTS</span></span>

### <span data-ttu-id="800c3-183">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="800c3-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="800c3-184">Notizen</span><span class="sxs-lookup"><span data-stu-id="800c3-184">NOTES</span></span>

## <span data-ttu-id="800c3-185">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="800c3-185">RELATED LINKS</span></span>

[<span data-ttu-id="800c3-186">Finden-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="800c3-186">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="800c3-187">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="800c3-187">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="800c3-188">Verschieben-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="800c3-188">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="800c3-189">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="800c3-189">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="800c3-190">Satz-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="800c3-190">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
