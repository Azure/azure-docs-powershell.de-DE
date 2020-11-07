---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
ms.openlocfilehash: 9b1f12060ca7cc161f4f7fbe7c99948d9ddd10f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664206"
---
# <span data-ttu-id="d0d1a-101">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d0d1a-101">Set-AzureRmResource</span></span>

## <span data-ttu-id="d0d1a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d0d1a-102">SYNOPSIS</span></span>
<span data-ttu-id="d0d1a-103">Ändert eine Ressource.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-103">Modifies a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0d1a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0d1a-104">SYNTAX</span></span>

### <span data-ttu-id="d0d1a-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="d0d1a-105">ByResourceId (Default)</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0d1a-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="d0d1a-106">BySubscriptionLevel</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0d1a-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="d0d1a-107">ByTenantLevel</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0d1a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d0d1a-108">DESCRIPTION</span></span>
<span data-ttu-id="d0d1a-109">Das Cmdlet " **Satz-AzureRmResource** " ändert eine vorhandene Azure-Ressource.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-109">The **Set-AzureRmResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="d0d1a-110">Geben Sie eine Ressource an, die nach Name und Typ oder nach ID geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-110">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="d0d1a-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d0d1a-111">EXAMPLES</span></span>

### <span data-ttu-id="d0d1a-112">Beispiel 1: Ändern einer Ressource</span><span class="sxs-lookup"><span data-stu-id="d0d1a-112">Example 1: Modify a resource</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoSite"
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzureRmResource -Force
```

<span data-ttu-id="d0d1a-113">Der erste Befehl ruft die Ressource mit dem Namen ContosoSite mithilfe des Get-AzureRmResource-Cmdlets ab und speichert Sie dann in der $Resource-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-113">The first command gets the resource named ContosoSite by using the Get-AzureRmResource cmdlet, and then stores it in the $Resource variable.</span></span>

<span data-ttu-id="d0d1a-114">Der zweite Befehl ändert eine Eigenschaft von $Resource.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-114">The second command modifies a property of $Resource.</span></span>

<span data-ttu-id="d0d1a-115">Mit dem letzten Befehl wird die Ressource so aktualisiert, dass Sie $Resource entspricht.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-115">The final command updates the resource to match $Resource.</span></span>

## <span data-ttu-id="d0d1a-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0d1a-116">PARAMETERS</span></span>

### <span data-ttu-id="d0d1a-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d0d1a-117">-ApiVersion</span></span>
<span data-ttu-id="d0d1a-118">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d0d1a-119">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d0d1a-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0d1a-120">-AsJob</span></span>
<span data-ttu-id="d0d1a-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d0d1a-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0d1a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0d1a-122">-DefaultProfile</span></span>
<span data-ttu-id="d0d1a-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d0d1a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0d1a-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="d0d1a-124">-ExtensionResourceName</span></span>
<span data-ttu-id="d0d1a-125">Gibt den Namen einer Erweiterungs Ressource für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-125">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="d0d1a-126">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="d0d1a-126">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="d0d1a-127">Name der Servernamen- `/` Datenbank</span><span class="sxs-lookup"><span data-stu-id="d0d1a-127">server name`/`database name</span></span>

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

### <span data-ttu-id="d0d1a-128">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="d0d1a-128">-ExtensionResourceType</span></span>
<span data-ttu-id="d0d1a-129">Gibt den Ressourcentyp für eine Erweiterungs Ressource an.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-129">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="d0d1a-130">Wenn beispielsweise die Erweiterungs Ressource eine Datenbank ist, geben Sie Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="d0d1a-130">For instance, if the extension resource is a database specify the following:</span></span>

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

### <span data-ttu-id="d0d1a-131">-Force</span><span class="sxs-lookup"><span data-stu-id="d0d1a-131">-Force</span></span>
<span data-ttu-id="d0d1a-132">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d0d1a-133">-Art</span><span class="sxs-lookup"><span data-stu-id="d0d1a-133">-Kind</span></span>
<span data-ttu-id="d0d1a-134">Gibt die Art der Ressource für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-134">Specifies the resource kind for the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0d1a-135">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="d0d1a-135">-ODataQuery</span></span>
<span data-ttu-id="d0d1a-136">Gibt einen Open Data Protocol (OData)-stilfilter an.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-136">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="d0d1a-137">Dieses Cmdlet fügt zusätzlich zu anderen Filtern diesen Wert an die Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-137">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="d0d1a-138">-Plan</span><span class="sxs-lookup"><span data-stu-id="d0d1a-138">-Plan</span></span>
<span data-ttu-id="d0d1a-139">Gibt Ressourcenplan Eigenschaften als Hashtabelle für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-139">Specifies resource plan properties, as a hash table, for the resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0d1a-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="d0d1a-140">-Pre</span></span>
<span data-ttu-id="d0d1a-141">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d0d1a-142">-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d0d1a-142">-Properties</span></span>
<span data-ttu-id="d0d1a-143">Gibt Ressourceneigenschaften für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-143">Specifies resource properties for the resource.</span></span>

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0d1a-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0d1a-144">-ResourceGroupName</span></span>
<span data-ttu-id="d0d1a-145">Gibt den Namen der Ressourcengruppe an, in der dieses Cmdlet die Ressource ändert.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-145">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="d0d1a-146">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d0d1a-146">-ResourceId</span></span>
<span data-ttu-id="d0d1a-147">Gibt die vollqualifizierte Ressourcen-ID an, einschließlich des Abonnements, wie im folgenden Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d0d1a-147">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="d0d1a-148">`/subscriptions/`Abonnement-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="d0d1a-148">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="d0d1a-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d0d1a-149">-ResourceName</span></span>
<span data-ttu-id="d0d1a-150">Gibt den Namen der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-150">Specifies the name of the resource.</span></span>
<span data-ttu-id="d0d1a-151">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="d0d1a-151">For instance, to specify a database, use the following format:</span></span>

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

### <span data-ttu-id="d0d1a-152">-</span><span class="sxs-lookup"><span data-stu-id="d0d1a-152">-ResourceType</span></span>
<span data-ttu-id="d0d1a-153">Gibt den Typ der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-153">Specifies the type of the resource.</span></span>
<span data-ttu-id="d0d1a-154">Bei einer Datenbank lautet der Ressourcentyp beispielsweise wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d0d1a-154">For instance, for a database, the resource type is as follows:</span></span>

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

### <span data-ttu-id="d0d1a-155">-SKU</span><span class="sxs-lookup"><span data-stu-id="d0d1a-155">-Sku</span></span>
<span data-ttu-id="d0d1a-156">Gibt das SKU-Objekt der Ressource als Hashtabelle an.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-156">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="d0d1a-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="d0d1a-157">-Tag</span></span>
<span data-ttu-id="d0d1a-158">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="d0d1a-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d0d1a-159">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d0d1a-159">For example:</span></span>

<span data-ttu-id="d0d1a-160">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="d0d1a-160">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0d1a-161">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="d0d1a-161">-TenantLevel</span></span>
<span data-ttu-id="d0d1a-162">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-162">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="d0d1a-163">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="d0d1a-163">-UsePatchSemantics</span></span>
<span data-ttu-id="d0d1a-164">Gibt an, dass dieses Cmdlet anstelle eines HTTP-PUT einen HTTP-Patch zum Aktualisieren des Objekts verwendet.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-164">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="d0d1a-165">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d0d1a-165">-Confirm</span></span>
<span data-ttu-id="d0d1a-166">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0d1a-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0d1a-167">-WhatIf</span></span>
<span data-ttu-id="d0d1a-168">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0d1a-169">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0d1a-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0d1a-170">CommonParameters</span></span>
<span data-ttu-id="d0d1a-171">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0d1a-172">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0d1a-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0d1a-173">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d0d1a-173">INPUTS</span></span>

### <span data-ttu-id="d0d1a-174">Keine</span><span class="sxs-lookup"><span data-stu-id="d0d1a-174">None</span></span>
<span data-ttu-id="d0d1a-175">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="d0d1a-175">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d0d1a-176">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d0d1a-176">OUTPUTS</span></span>

### <span data-ttu-id="d0d1a-177">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d0d1a-177">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d0d1a-178">Notizen</span><span class="sxs-lookup"><span data-stu-id="d0d1a-178">NOTES</span></span>

## <span data-ttu-id="d0d1a-179">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d0d1a-179">RELATED LINKS</span></span>

[<span data-ttu-id="d0d1a-180">Finden-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d0d1a-180">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="d0d1a-181">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d0d1a-181">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="d0d1a-182">Verschieben-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d0d1a-182">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="d0d1a-183">Neu – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d0d1a-183">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="d0d1a-184">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d0d1a-184">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)
