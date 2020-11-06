---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BB90E6BB-7F53-4441-A7B2-EDA940621D49
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
ms.openlocfilehash: e626a57088a9c726bfe9040f76157f0b011a6405
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481629"
---
# <span data-ttu-id="09355-101">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="09355-101">Find-AzureRmResource</span></span>

## <span data-ttu-id="09355-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="09355-102">SYNOPSIS</span></span>
<span data-ttu-id="09355-103">Sucht nach Ressourcen auf der Grundlage der angegebenen Parameter.</span><span class="sxs-lookup"><span data-stu-id="09355-103">Searches for resources based on specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09355-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="09355-104">SYNTAX</span></span>

### <span data-ttu-id="09355-105">Listet die Ressourcen auf Grundlage des angegebenen Bereichs auf.</span><span class="sxs-lookup"><span data-stu-id="09355-105">Lists the resources based on the specified scope.</span></span> <span data-ttu-id="09355-106">Standard</span><span class="sxs-lookup"><span data-stu-id="09355-106">(Default)</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] [-ResourceType <String>]
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="09355-107">Listet die Ressourcen auf der Grundlage des angegebenen Bereichs auf Mandantenebene auf.</span><span class="sxs-lookup"><span data-stu-id="09355-107">Lists the resources based on the specified scope at the tenant level.</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ExpandProperties] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="09355-108">Abrufen von Ressourcen mithilfe einer Abfrage mit mehreren Abonnements</span><span class="sxs-lookup"><span data-stu-id="09355-108">Get a resources using a multi-subscription query.</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="09355-109">Listet Ressourcen nach einem als HashSet angegebenen Tag-Objekt auf.</span><span class="sxs-lookup"><span data-stu-id="09355-109">Lists resources by a tag object specified as a hashset.</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-Tag <Hashtable>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="09355-110">Listet Ressourcen nach einem Tag auf, das als einzelne Name-und Wertparameter angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="09355-110">Lists resources by a tag specified as a individual name and value parameters.</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-TagName <String>] [-TagValue <String>]
 [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="09355-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09355-111">DESCRIPTION</span></span>
<span data-ttu-id="09355-112">Das Cmdlet " **Suchen-AzureRmResource** " sucht nach Ressourcen auf der Grundlage der angegebenen Parameter.</span><span class="sxs-lookup"><span data-stu-id="09355-112">The **Find-AzureRmResource** cmdlet searches for resources based on specified parameters.</span></span>

## <span data-ttu-id="09355-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09355-113">EXAMPLES</span></span>

### <span data-ttu-id="09355-114">Beispiel 1: Suchen nach Ressourcen nach Typ und Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="09355-114">Example 1: Search for resources by type and resource group name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupNameContains "ResourceGroup"
```

<span data-ttu-id="09355-115">Dieser Befehl sucht nach Ressourcen des Typs "Microsoft. Web/Websites" unter "Ressourcengruppen", deren Namen mit der Zeichenfolge "ResourceGroup" übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="09355-115">This command searches for resources of the type microsoft.web/sites under resource groups that have names that match the string ResourceGroup.</span></span>

### <span data-ttu-id="09355-116">Beispiel 2: Suchen nach Ressourcen nach Typ und Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="09355-116">Example 2: Search for resources by type and resource name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceNameContains "test"
```

<span data-ttu-id="09355-117">Dieser Befehl sucht nach Ressourcen des Typs Microsoft. Web/Websites mit einem Ressourcennamen, der dem Zeichenfolgentest entspricht.</span><span class="sxs-lookup"><span data-stu-id="09355-117">This command searches for resources of the type microsoft.web/sites that have a resource name that matches the string test.</span></span>

## <span data-ttu-id="09355-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="09355-118">PARAMETERS</span></span>

### <span data-ttu-id="09355-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="09355-119">-ApiVersion</span></span>
<span data-ttu-id="09355-120">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="09355-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="09355-121">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="09355-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="09355-122">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="09355-122">-ExpandProperties</span></span>
<span data-ttu-id="09355-123">Gibt an, dass dieses Cmdlet die Eigenschaften der Ressource erweitert.</span><span class="sxs-lookup"><span data-stu-id="09355-123">Indicates that this cmdlet expands the properties of the resource.</span></span>

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

### <span data-ttu-id="09355-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="09355-124">-ExtensionResourceType</span></span>
<span data-ttu-id="09355-125">Gibt den Erweiterungs Ressourcentyp für die Ressourcen an, für die dieses Cmdlet durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="09355-125">Specifies the extension resource type for the resources for which this cmdlet searches.</span></span>
<span data-ttu-id="09355-126">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="09355-126">For instance:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09355-127">-Information</span><span class="sxs-lookup"><span data-stu-id="09355-127">-InformationAction</span></span>
<span data-ttu-id="09355-128">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="09355-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="09355-129">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="09355-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="09355-130">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="09355-130">Continue</span></span>
- <span data-ttu-id="09355-131">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="09355-131">Ignore</span></span>
- <span data-ttu-id="09355-132">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="09355-132">Inquire</span></span>
- <span data-ttu-id="09355-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="09355-133">SilentlyContinue</span></span>
- <span data-ttu-id="09355-134">Beenden</span><span class="sxs-lookup"><span data-stu-id="09355-134">Stop</span></span>
- <span data-ttu-id="09355-135">Anhalten</span><span class="sxs-lookup"><span data-stu-id="09355-135">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09355-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="09355-136">-InformationVariable</span></span>
<span data-ttu-id="09355-137">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="09355-137">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09355-138">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="09355-138">-ODataQuery</span></span>
<span data-ttu-id="09355-139">Gibt einen Open Data Protocol (OData)-stilfilter an.</span><span class="sxs-lookup"><span data-stu-id="09355-139">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="09355-140">Dieses Cmdlet fügt zusätzlich zu anderen Filtern diesen Wert an die Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="09355-140">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="09355-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="09355-141">-Pre</span></span>
<span data-ttu-id="09355-142">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="09355-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="09355-143">-ResourceGroupNameContains</span><span class="sxs-lookup"><span data-stu-id="09355-143">-ResourceGroupNameContains</span></span>
<span data-ttu-id="09355-144">Gibt einen partiellen Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="09355-144">Specifies a partial name of a resource group.</span></span>
<span data-ttu-id="09355-145">Dieses Cmdlet entspricht Ressourcengruppen, für die dieser Wert eine Teilzeichenfolge ist.</span><span class="sxs-lookup"><span data-stu-id="09355-145">This cmdlet matches resource groups of which this value is a substring.</span></span>
<span data-ttu-id="09355-146">Das Cmdlet sucht nach Ressourcen in diesen Ressourcengruppen.</span><span class="sxs-lookup"><span data-stu-id="09355-146">The cmdlet searches for resources in those resource groups.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Get a resources using a multi-subscription query.
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09355-147">-ResourceGroupNameEquals</span><span class="sxs-lookup"><span data-stu-id="09355-147">-ResourceGroupNameEquals</span></span>
<span data-ttu-id="09355-148">Der Name der Ressourcengruppe für eine vollständige Übereinstimmung.</span><span class="sxs-lookup"><span data-stu-id="09355-148">The resource group name for a full match.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09355-149">-ResourceNameContains</span><span class="sxs-lookup"><span data-stu-id="09355-149">-ResourceNameContains</span></span>
<span data-ttu-id="09355-150">Gibt einen partiellen Namen einer Ressource an.</span><span class="sxs-lookup"><span data-stu-id="09355-150">Specifies a partial name of a resource.</span></span>
<span data-ttu-id="09355-151">Das Cmdlet sucht nach Ressourcen, die diesen Wert als Teilzeichenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="09355-151">The cmdlet searches for resources which contain this value as a substring.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09355-152">-ResourceNameEquals</span><span class="sxs-lookup"><span data-stu-id="09355-152">-ResourceNameEquals</span></span>
<span data-ttu-id="09355-153">Der Ressourcenname für eine vollständige Übereinstimmung.</span><span class="sxs-lookup"><span data-stu-id="09355-153">The resource name for a full match.</span></span> <span data-ttu-id="09355-154">Wenn Ihr Ressourcenname z.b. testResource ist, können Sie testResource angeben.</span><span class="sxs-lookup"><span data-stu-id="09355-154">e.g. if your resource name is testResource, you can specify testResource.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09355-155">-</span><span class="sxs-lookup"><span data-stu-id="09355-155">-ResourceType</span></span>
<span data-ttu-id="09355-156">Gibt den Typ einer Ressource an.</span><span class="sxs-lookup"><span data-stu-id="09355-156">Specifies the type of a resource.</span></span>
<span data-ttu-id="09355-157">Bei einer Datenbank lautet der Ressourcentyp beispielsweise wie folgt:</span><span class="sxs-lookup"><span data-stu-id="09355-157">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

<span data-ttu-id="09355-158">Dieses Cmdlet sucht nach Ressourcen des angegebenen Typs.</span><span class="sxs-lookup"><span data-stu-id="09355-158">This cmdlet searches for resources of the specified type.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09355-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="09355-159">-Tag</span></span>
<span data-ttu-id="09355-160">Der Transponder Filter für die OData-Abfrage.</span><span class="sxs-lookup"><span data-stu-id="09355-160">The tag filter for the OData query.</span></span> <span data-ttu-id="09355-161">Das erwartete Format ist @ {Tagname = $NULL} oder @ {Tagname = ' tagValue '}.</span><span class="sxs-lookup"><span data-stu-id="09355-161">The expected format is @{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Lists resources by a tag object specified as a hashset.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09355-162">-Tagname</span><span class="sxs-lookup"><span data-stu-id="09355-162">-TagName</span></span>
```yaml
Type: System.String
Parameter Sets: Lists resources by a tag specified as a individual name and value parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09355-163">-TagValue</span><span class="sxs-lookup"><span data-stu-id="09355-163">-TagValue</span></span>
```yaml
Type: System.String
Parameter Sets: Lists resources by a tag specified as a individual name and value parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09355-164">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="09355-164">-TenantLevel</span></span>
<span data-ttu-id="09355-165">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="09355-165">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09355-166">-Top</span><span class="sxs-lookup"><span data-stu-id="09355-166">-Top</span></span>
<span data-ttu-id="09355-167">Gibt die Anzahl der Ressourcen an, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="09355-167">Specifies the number of resources to retrieve.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09355-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09355-168">-DefaultProfile</span></span>
<span data-ttu-id="09355-169">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="09355-169">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09355-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09355-170">CommonParameters</span></span>
<span data-ttu-id="09355-171">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09355-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09355-172">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09355-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09355-173">Eingaben</span><span class="sxs-lookup"><span data-stu-id="09355-173">INPUTS</span></span>

## <span data-ttu-id="09355-174">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="09355-174">OUTPUTS</span></span>

### <span data-ttu-id="09355-175">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="09355-175">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="09355-176">Notizen</span><span class="sxs-lookup"><span data-stu-id="09355-176">NOTES</span></span>

## <span data-ttu-id="09355-177">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="09355-177">RELATED LINKS</span></span>

[<span data-ttu-id="09355-178">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="09355-178">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="09355-179">Verschieben-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="09355-179">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="09355-180">Neu – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="09355-180">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="09355-181">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="09355-181">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="09355-182">Satz-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="09355-182">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
