---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
ms.openlocfilehash: eb75c1afc0b0fa82c0fee6b734ded951fdfa519f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501638"
---
# <span data-ttu-id="8cf74-101">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8cf74-101">New-AzureRmResource</span></span>

## <span data-ttu-id="8cf74-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8cf74-102">SYNOPSIS</span></span>
<span data-ttu-id="8cf74-103">Erstellt eine Ressource.</span><span class="sxs-lookup"><span data-stu-id="8cf74-103">Creates a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cf74-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cf74-104">SYNTAX</span></span>

### <span data-ttu-id="8cf74-105">Die Ressourcen-ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="8cf74-105">The resource Id. (Default)</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8cf74-106">Die Ressource, die sich auf der Abonnementebene befindet.</span><span class="sxs-lookup"><span data-stu-id="8cf74-106">Resource that resides at the subscription level.</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cf74-107">Die Ressource, die sich auf der Mandantenebene befindet.</span><span class="sxs-lookup"><span data-stu-id="8cf74-107">Resource that resides at the tenant level.</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8cf74-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cf74-108">DESCRIPTION</span></span>
<span data-ttu-id="8cf74-109">Das Cmdlet **New-AzureRmResource** erstellt eine Azure-Ressource, beispielsweise eine Website, einen Azure SQL-Datenbankserver oder eine Azure SQL-Datenbank, in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8cf74-109">The **New-AzureRmResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="8cf74-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8cf74-110">EXAMPLES</span></span>

### <span data-ttu-id="8cf74-111">Beispiel 1: Erstellen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="8cf74-111">Example 1: Create a resource</span></span>
```
PS C:\>New-AzureRmResource -Location "West US" -Properties @{"test"="test"} -ResourceName "TestSite06" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -Force
```

<span data-ttu-id="8cf74-112">Mit diesem Befehl wird eine Ressource erstellt, bei der es sich um eine Website in ResourceGroup11 handelt.</span><span class="sxs-lookup"><span data-stu-id="8cf74-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="8cf74-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cf74-113">PARAMETERS</span></span>

### <span data-ttu-id="8cf74-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8cf74-114">-ApiVersion</span></span>
<span data-ttu-id="8cf74-115">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="8cf74-115">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="8cf74-116">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="8cf74-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8cf74-117">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="8cf74-117">-ExtensionResourceName</span></span>
<span data-ttu-id="8cf74-118">Gibt den Namen einer Erweiterungs Ressource für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="8cf74-118">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="8cf74-119">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="8cf74-119">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="8cf74-120">Name der Servernamen- `/` Datenbank</span><span class="sxs-lookup"><span data-stu-id="8cf74-120">server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cf74-121">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="8cf74-121">-ExtensionResourceType</span></span>
<span data-ttu-id="8cf74-122">Gibt den Ressourcentyp für eine Erweiterungs Ressource an.</span><span class="sxs-lookup"><span data-stu-id="8cf74-122">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="8cf74-123">Wenn es sich bei der Erweiterungs Ressource beispielsweise um eine Datenbank handelt, geben Sie den folgenden Typ an:</span><span class="sxs-lookup"><span data-stu-id="8cf74-123">For instance, if the extension resource is a database, specify the following type:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cf74-124">-Force</span><span class="sxs-lookup"><span data-stu-id="8cf74-124">-Force</span></span>
<span data-ttu-id="8cf74-125">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="8cf74-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8cf74-126">-Isfullobject</span><span class="sxs-lookup"><span data-stu-id="8cf74-126">-IsFullObject</span></span>
<span data-ttu-id="8cf74-127">Gibt an, dass das Objekt, das der *Properties* -Parameter angibt, das vollständige Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="8cf74-127">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="8cf74-128">-Art</span><span class="sxs-lookup"><span data-stu-id="8cf74-128">-Kind</span></span>
<span data-ttu-id="8cf74-129">Gibt die Art der Ressource für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="8cf74-129">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="8cf74-130">-Standort</span><span class="sxs-lookup"><span data-stu-id="8cf74-130">-Location</span></span>
<span data-ttu-id="8cf74-131">Gibt den Speicherort der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="8cf74-131">Specifies the location of the resource.</span></span>
<span data-ttu-id="8cf74-132">Geben Sie den Speicherort des Datencenters an, beispielsweise Zentralamerika oder Südostasien.</span><span class="sxs-lookup"><span data-stu-id="8cf74-132">Specify data center location, such as Central US or Southeast Asia.</span></span>

<span data-ttu-id="8cf74-133">Sie können eine Ressource an einem beliebigen Speicherort platzieren, der Ressourcen dieses Typs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8cf74-133">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="8cf74-134">Ressourcengruppen können Ressourcen aus unterschiedlichen Speicherorten enthalten.</span><span class="sxs-lookup"><span data-stu-id="8cf74-134">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="8cf74-135">Verwenden Sie das Get-AzureLocation-Cmdlet, um zu ermitteln, welche Speicherorte die einzelnen Ressourcentypen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8cf74-135">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

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

### <span data-ttu-id="8cf74-136">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="8cf74-136">-ODataQuery</span></span>
<span data-ttu-id="8cf74-137">Gibt einen Open Data Protocol (OData)-stilfilter an.</span><span class="sxs-lookup"><span data-stu-id="8cf74-137">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="8cf74-138">Dieses Cmdlet fügt zusätzlich zu anderen Filtern diesen Wert an die Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="8cf74-138">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="8cf74-139">-Plan</span><span class="sxs-lookup"><span data-stu-id="8cf74-139">-Plan</span></span>
<span data-ttu-id="8cf74-140">Eine Hashtabelle, die Ressourcenplan Eigenschaften darstellt.</span><span class="sxs-lookup"><span data-stu-id="8cf74-140">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="8cf74-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="8cf74-141">-Pre</span></span>
<span data-ttu-id="8cf74-142">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="8cf74-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8cf74-143">-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8cf74-143">-Properties</span></span>
<span data-ttu-id="8cf74-144">Gibt Ressourceneigenschaften für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="8cf74-144">Specifies resource properties for the resource.</span></span> <span data-ttu-id="8cf74-145">Verwenden Sie diesen Parameter, um die Werte von Eigenschaften anzugeben, die für einen Ressourcentyp spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="8cf74-145">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="8cf74-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cf74-146">-ResourceGroupName</span></span>
<span data-ttu-id="8cf74-147">Gibt den Namen der Ressourcengruppe an, in der dieses Cmdlet die Ressource erstellt.</span><span class="sxs-lookup"><span data-stu-id="8cf74-147">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cf74-148">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8cf74-148">-ResourceId</span></span>
<span data-ttu-id="8cf74-149">Gibt die vollqualifizierte Ressourcen-ID an, einschließlich des Abonnements, wie im folgenden Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8cf74-149">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="8cf74-150">`/subscriptions/`Abonnement-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="8cf74-150">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: The resource Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cf74-151">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8cf74-151">-ResourceName</span></span>
<span data-ttu-id="8cf74-152">Gibt den Namen der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="8cf74-152">Specifies the name of the resource.</span></span> <span data-ttu-id="8cf74-153">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="8cf74-153">For instance, to specify a database, use the following format:</span></span>

`ContosoServer/ContosoDatabase`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cf74-154">-</span><span class="sxs-lookup"><span data-stu-id="8cf74-154">-ResourceType</span></span>
<span data-ttu-id="8cf74-155">Gibt den Typ der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="8cf74-155">Specifies the type of the resource.</span></span>
<span data-ttu-id="8cf74-156">Bei einer Datenbank lautet der Ressourcentyp beispielsweise wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8cf74-156">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cf74-157">-SKU</span><span class="sxs-lookup"><span data-stu-id="8cf74-157">-Sku</span></span>
<span data-ttu-id="8cf74-158">Eine Hashtabelle, die SKU-Eigenschaften darstellt.</span><span class="sxs-lookup"><span data-stu-id="8cf74-158">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="8cf74-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="8cf74-159">-Tag</span></span>
<span data-ttu-id="8cf74-160">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="8cf74-160">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8cf74-161">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8cf74-161">For example:</span></span>

<span data-ttu-id="8cf74-162">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="8cf74-162">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8cf74-163">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="8cf74-163">-TenantLevel</span></span>
<span data-ttu-id="8cf74-164">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="8cf74-164">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf74-165">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8cf74-165">-Confirm</span></span>
<span data-ttu-id="8cf74-166">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8cf74-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cf74-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cf74-167">-WhatIf</span></span>
<span data-ttu-id="8cf74-168">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8cf74-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cf74-169">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8cf74-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cf74-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cf74-170">-DefaultProfile</span></span>
<span data-ttu-id="8cf74-171">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8cf74-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cf74-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cf74-172">CommonParameters</span></span>
<span data-ttu-id="8cf74-173">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cf74-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cf74-174">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cf74-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cf74-175">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8cf74-175">INPUTS</span></span>

## <span data-ttu-id="8cf74-176">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8cf74-176">OUTPUTS</span></span>

### <span data-ttu-id="8cf74-177">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="8cf74-177">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8cf74-178">Notizen</span><span class="sxs-lookup"><span data-stu-id="8cf74-178">NOTES</span></span>

## <span data-ttu-id="8cf74-179">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8cf74-179">RELATED LINKS</span></span>

[<span data-ttu-id="8cf74-180">Finden-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8cf74-180">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="8cf74-181">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8cf74-181">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="8cf74-182">Verschieben-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8cf74-182">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="8cf74-183">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8cf74-183">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="8cf74-184">Satz-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8cf74-184">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
