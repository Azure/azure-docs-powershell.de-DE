---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
ms.openlocfilehash: d3e7a1e947eb03c52c2cd8e032a359eb7765be03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664440"
---
# <span data-ttu-id="c717a-101">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c717a-101">Set-AzureRmResource</span></span>

## <span data-ttu-id="c717a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c717a-102">SYNOPSIS</span></span>
<span data-ttu-id="c717a-103">Ändert eine Ressource.</span><span class="sxs-lookup"><span data-stu-id="c717a-103">Modifies a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c717a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c717a-104">SYNTAX</span></span>

### <span data-ttu-id="c717a-105">Die Ressourcen-ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="c717a-105">The resource Id. (Default)</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c717a-106">Die Ressource, die sich auf der Abonnementebene befindet.</span><span class="sxs-lookup"><span data-stu-id="c717a-106">Resource that resides at the subscription level.</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c717a-107">Die Ressource, die sich auf der Mandantenebene befindet.</span><span class="sxs-lookup"><span data-stu-id="c717a-107">Resource that resides at the tenant level.</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c717a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c717a-108">DESCRIPTION</span></span>
<span data-ttu-id="c717a-109">Das Cmdlet " **Satz-AzureRmResource** " ändert eine vorhandene Azure-Ressource.</span><span class="sxs-lookup"><span data-stu-id="c717a-109">The **Set-AzureRmResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="c717a-110">Geben Sie eine Ressource an, die nach Name und Typ oder nach ID geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c717a-110">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="c717a-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c717a-111">EXAMPLES</span></span>

### <span data-ttu-id="c717a-112">Beispiel 1: Ändern einer Ressource</span><span class="sxs-lookup"><span data-stu-id="c717a-112">Example 1: Modify a resource</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoSite"
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzureRmResource -Force
```

<span data-ttu-id="c717a-113">Der erste Befehl ruft die Ressource mit dem Namen ContosoSite mithilfe des Get-AzureRmResource-Cmdlets ab und speichert Sie dann in der $Resource-Variablen.</span><span class="sxs-lookup"><span data-stu-id="c717a-113">The first command gets the resource named ContosoSite by using the Get-AzureRmResource cmdlet, and then stores it in the $Resource variable.</span></span>

<span data-ttu-id="c717a-114">Der zweite Befehl ändert eine Eigenschaft von $Resource.</span><span class="sxs-lookup"><span data-stu-id="c717a-114">The second command modifies a property of $Resource.</span></span>

<span data-ttu-id="c717a-115">Mit dem letzten Befehl wird die Ressource so aktualisiert, dass Sie $Resource entspricht.</span><span class="sxs-lookup"><span data-stu-id="c717a-115">The final command updates the resource to match $Resource.</span></span>

## <span data-ttu-id="c717a-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="c717a-116">PARAMETERS</span></span>

### <span data-ttu-id="c717a-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c717a-117">-ApiVersion</span></span>
<span data-ttu-id="c717a-118">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="c717a-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c717a-119">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="c717a-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c717a-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="c717a-120">-ExtensionResourceName</span></span>
<span data-ttu-id="c717a-121">Gibt den Namen einer Erweiterungs Ressource für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="c717a-121">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="c717a-122">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="c717a-122">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="c717a-123">Name der Servernamen- `/` Datenbank</span><span class="sxs-lookup"><span data-stu-id="c717a-123">server name`/`database name</span></span>

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

### <span data-ttu-id="c717a-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="c717a-124">-ExtensionResourceType</span></span>
<span data-ttu-id="c717a-125">Gibt den Ressourcentyp für eine Erweiterungs Ressource an.</span><span class="sxs-lookup"><span data-stu-id="c717a-125">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="c717a-126">Wenn beispielsweise die Erweiterungs Ressource eine Datenbank ist, geben Sie Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="c717a-126">For instance, if the extension resource is a database specify the following:</span></span>

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

### <span data-ttu-id="c717a-127">-Force</span><span class="sxs-lookup"><span data-stu-id="c717a-127">-Force</span></span>
<span data-ttu-id="c717a-128">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="c717a-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c717a-129">-Art</span><span class="sxs-lookup"><span data-stu-id="c717a-129">-Kind</span></span>
<span data-ttu-id="c717a-130">Gibt die Art der Ressource für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="c717a-130">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="c717a-131">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="c717a-131">-ODataQuery</span></span>
<span data-ttu-id="c717a-132">Gibt einen Open Data Protocol (OData)-stilfilter an.</span><span class="sxs-lookup"><span data-stu-id="c717a-132">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="c717a-133">Dieses Cmdlet fügt zusätzlich zu anderen Filtern diesen Wert an die Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="c717a-133">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="c717a-134">-Plan</span><span class="sxs-lookup"><span data-stu-id="c717a-134">-Plan</span></span>
<span data-ttu-id="c717a-135">Gibt Ressourcenplan Eigenschaften als Hashtabelle für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="c717a-135">Specifies resource plan properties, as a hash table, for the resource.</span></span>

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

### <span data-ttu-id="c717a-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="c717a-136">-Pre</span></span>
<span data-ttu-id="c717a-137">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c717a-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c717a-138">-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c717a-138">-Properties</span></span>
<span data-ttu-id="c717a-139">Gibt Ressourceneigenschaften für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="c717a-139">Specifies resource properties for the resource.</span></span>

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

### <span data-ttu-id="c717a-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c717a-140">-ResourceGroupName</span></span>
<span data-ttu-id="c717a-141">Gibt den Namen der Ressourcengruppe an, in der dieses Cmdlet die Ressource ändert.</span><span class="sxs-lookup"><span data-stu-id="c717a-141">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="c717a-142">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c717a-142">-ResourceId</span></span>
<span data-ttu-id="c717a-143">Gibt die vollqualifizierte Ressourcen-ID an, einschließlich des Abonnements, wie im folgenden Beispiel:</span><span class="sxs-lookup"><span data-stu-id="c717a-143">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="c717a-144">`/subscriptions/`Abonnement-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="c717a-144">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="c717a-145">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c717a-145">-ResourceName</span></span>
<span data-ttu-id="c717a-146">Gibt den Namen der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="c717a-146">Specifies the name of the resource.</span></span>
<span data-ttu-id="c717a-147">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="c717a-147">For instance, to specify a database, use the following format:</span></span>

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

### <span data-ttu-id="c717a-148">-</span><span class="sxs-lookup"><span data-stu-id="c717a-148">-ResourceType</span></span>
<span data-ttu-id="c717a-149">Gibt den Typ der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="c717a-149">Specifies the type of the resource.</span></span>
<span data-ttu-id="c717a-150">Bei einer Datenbank lautet der Ressourcentyp beispielsweise wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c717a-150">For instance, for a database, the resource type is as follows:</span></span>

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

### <span data-ttu-id="c717a-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="c717a-151">-Sku</span></span>
<span data-ttu-id="c717a-152">Gibt das SKU-Objekt der Ressource als Hashtabelle an.</span><span class="sxs-lookup"><span data-stu-id="c717a-152">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="c717a-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="c717a-153">-Tag</span></span>
<span data-ttu-id="c717a-154">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="c717a-154">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c717a-155">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="c717a-155">For example:</span></span>

<span data-ttu-id="c717a-156">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="c717a-156">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c717a-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="c717a-157">-TenantLevel</span></span>
<span data-ttu-id="c717a-158">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="c717a-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="c717a-159">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="c717a-159">-UsePatchSemantics</span></span>
<span data-ttu-id="c717a-160">Gibt an, dass dieses Cmdlet anstelle eines HTTP-PUT einen HTTP-Patch zum Aktualisieren des Objekts verwendet.</span><span class="sxs-lookup"><span data-stu-id="c717a-160">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="c717a-161">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c717a-161">-Confirm</span></span>
<span data-ttu-id="c717a-162">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c717a-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c717a-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c717a-163">-WhatIf</span></span>
<span data-ttu-id="c717a-164">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c717a-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c717a-165">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c717a-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c717a-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c717a-166">-DefaultProfile</span></span>
<span data-ttu-id="c717a-167">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c717a-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c717a-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c717a-168">CommonParameters</span></span>
<span data-ttu-id="c717a-169">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c717a-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c717a-170">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c717a-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c717a-171">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c717a-171">INPUTS</span></span>

## <span data-ttu-id="c717a-172">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c717a-172">OUTPUTS</span></span>

### <span data-ttu-id="c717a-173">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c717a-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c717a-174">Notizen</span><span class="sxs-lookup"><span data-stu-id="c717a-174">NOTES</span></span>

## <span data-ttu-id="c717a-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c717a-175">RELATED LINKS</span></span>

[<span data-ttu-id="c717a-176">Finden-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c717a-176">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="c717a-177">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c717a-177">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="c717a-178">Verschieben-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c717a-178">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="c717a-179">Neu – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c717a-179">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="c717a-180">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c717a-180">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)
