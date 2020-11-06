---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BB90E6BB-7F53-4441-A7B2-EDA940621D49
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/find-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
ms.openlocfilehash: 67389829eb5edc5ea7ac21fcc891cc85787b5e9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498873"
---
# <span data-ttu-id="613a0-101">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="613a0-101">Find-AzureRmResource</span></span>

## <span data-ttu-id="613a0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="613a0-102">SYNOPSIS</span></span>
<span data-ttu-id="613a0-103">Sucht nach Ressourcen auf der Grundlage der angegebenen Parameter.</span><span class="sxs-lookup"><span data-stu-id="613a0-103">Searches for resources based on specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="613a0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="613a0-104">SYNTAX</span></span>

### <span data-ttu-id="613a0-105">GetBySpecifiedScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="613a0-105">GetBySpecifiedScope (Default)</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] [-ResourceType <String>]
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="613a0-106">GetBySpecifiedScopeAtTenantLevel</span><span class="sxs-lookup"><span data-stu-id="613a0-106">GetBySpecifiedScopeAtTenantLevel</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ExpandProperties] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="613a0-107">GetByMultiSubscriptionQuery</span><span class="sxs-lookup"><span data-stu-id="613a0-107">GetByMultiSubscriptionQuery</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="613a0-108">GetByTagObject</span><span class="sxs-lookup"><span data-stu-id="613a0-108">GetByTagObject</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-Tag <Hashtable>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="613a0-109">GetByTagNameValue</span><span class="sxs-lookup"><span data-stu-id="613a0-109">GetByTagNameValue</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-TagName <String>] [-TagValue <String>]
 [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="613a0-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="613a0-110">DESCRIPTION</span></span>
<span data-ttu-id="613a0-111">Das Cmdlet " **Suchen-AzureRmResource** " sucht nach Ressourcen auf der Grundlage der angegebenen Parameter.</span><span class="sxs-lookup"><span data-stu-id="613a0-111">The **Find-AzureRmResource** cmdlet searches for resources based on specified parameters.</span></span>

## <span data-ttu-id="613a0-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="613a0-112">EXAMPLES</span></span>

### <span data-ttu-id="613a0-113">Beispiel 1: Suchen nach Ressourcen nach Typ und Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="613a0-113">Example 1: Search for resources by type and resource group name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupNameContains "ResourceGroup"
```

<span data-ttu-id="613a0-114">Dieser Befehl sucht nach Ressourcen des Typs "Microsoft. Web/Websites" unter "Ressourcengruppen", deren Namen mit der Zeichenfolge "ResourceGroup" übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="613a0-114">This command searches for resources of the type microsoft.web/sites under resource groups that have names that match the string ResourceGroup.</span></span>

### <span data-ttu-id="613a0-115">Beispiel 2: Suchen nach Ressourcen nach Typ und Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="613a0-115">Example 2: Search for resources by type and resource name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceNameContains "test"
```

<span data-ttu-id="613a0-116">Dieser Befehl sucht nach Ressourcen des Typs Microsoft. Web/Websites mit einem Ressourcennamen, der dem Zeichenfolgentest entspricht.</span><span class="sxs-lookup"><span data-stu-id="613a0-116">This command searches for resources of the type microsoft.web/sites that have a resource name that matches the string test.</span></span>

## <span data-ttu-id="613a0-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="613a0-117">PARAMETERS</span></span>

### <span data-ttu-id="613a0-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="613a0-118">-ApiVersion</span></span>
<span data-ttu-id="613a0-119">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="613a0-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="613a0-120">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="613a0-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="613a0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="613a0-121">-DefaultProfile</span></span>
<span data-ttu-id="613a0-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="613a0-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="613a0-123">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="613a0-123">-ExpandProperties</span></span>
<span data-ttu-id="613a0-124">Gibt an, dass dieses Cmdlet die Eigenschaften der Ressource erweitert.</span><span class="sxs-lookup"><span data-stu-id="613a0-124">Indicates that this cmdlet expands the properties of the resource.</span></span>

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

### <span data-ttu-id="613a0-125">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="613a0-125">-ExtensionResourceType</span></span>
<span data-ttu-id="613a0-126">Gibt den Erweiterungs Ressourcentyp für die Ressourcen an, für die dieses Cmdlet durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="613a0-126">Specifies the extension resource type for the resources for which this cmdlet searches.</span></span>
<span data-ttu-id="613a0-127">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="613a0-127">For instance:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="613a0-128">-Information</span><span class="sxs-lookup"><span data-stu-id="613a0-128">-InformationAction</span></span>
<span data-ttu-id="613a0-129">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="613a0-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="613a0-130">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="613a0-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="613a0-131">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="613a0-131">Continue</span></span>
- <span data-ttu-id="613a0-132">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="613a0-132">Ignore</span></span>
- <span data-ttu-id="613a0-133">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="613a0-133">Inquire</span></span>
- <span data-ttu-id="613a0-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="613a0-134">SilentlyContinue</span></span>
- <span data-ttu-id="613a0-135">Beenden</span><span class="sxs-lookup"><span data-stu-id="613a0-135">Stop</span></span>
- <span data-ttu-id="613a0-136">Anhalten</span><span class="sxs-lookup"><span data-stu-id="613a0-136">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="613a0-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="613a0-137">-InformationVariable</span></span>
<span data-ttu-id="613a0-138">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="613a0-138">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="613a0-139">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="613a0-139">-ODataQuery</span></span>
<span data-ttu-id="613a0-140">Gibt einen Open Data Protocol (OData)-stilfilter an.</span><span class="sxs-lookup"><span data-stu-id="613a0-140">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="613a0-141">Dieses Cmdlet fügt zusätzlich zu anderen Filtern diesen Wert an die Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="613a0-141">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="613a0-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="613a0-142">-Pre</span></span>
<span data-ttu-id="613a0-143">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="613a0-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="613a0-144">-ResourceGroupNameContains</span><span class="sxs-lookup"><span data-stu-id="613a0-144">-ResourceGroupNameContains</span></span>
<span data-ttu-id="613a0-145">Gibt einen partiellen Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="613a0-145">Specifies a partial name of a resource group.</span></span>
<span data-ttu-id="613a0-146">Dieses Cmdlet entspricht Ressourcengruppen, für die dieser Wert eine Teilzeichenfolge ist.</span><span class="sxs-lookup"><span data-stu-id="613a0-146">This cmdlet matches resource groups of which this value is a substring.</span></span>
<span data-ttu-id="613a0-147">Das Cmdlet sucht nach Ressourcen in diesen Ressourcengruppen.</span><span class="sxs-lookup"><span data-stu-id="613a0-147">The cmdlet searches for resources in those resource groups.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetByMultiSubscriptionQuery
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="613a0-148">-ResourceGroupNameEquals</span><span class="sxs-lookup"><span data-stu-id="613a0-148">-ResourceGroupNameEquals</span></span>
<span data-ttu-id="613a0-149">Der Name der Ressourcengruppe für eine vollständige Übereinstimmung.</span><span class="sxs-lookup"><span data-stu-id="613a0-149">The resource group name for a full match.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="613a0-150">-ResourceNameContains</span><span class="sxs-lookup"><span data-stu-id="613a0-150">-ResourceNameContains</span></span>
<span data-ttu-id="613a0-151">Gibt einen partiellen Namen einer Ressource an.</span><span class="sxs-lookup"><span data-stu-id="613a0-151">Specifies a partial name of a resource.</span></span>
<span data-ttu-id="613a0-152">Das Cmdlet sucht nach Ressourcen, die diesen Wert als Teilzeichenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="613a0-152">The cmdlet searches for resources which contain this value as a substring.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="613a0-153">-ResourceNameEquals</span><span class="sxs-lookup"><span data-stu-id="613a0-153">-ResourceNameEquals</span></span>
<span data-ttu-id="613a0-154">Der Ressourcenname für eine vollständige Übereinstimmung.</span><span class="sxs-lookup"><span data-stu-id="613a0-154">The resource name for a full match.</span></span> <span data-ttu-id="613a0-155">Wenn Ihr Ressourcenname z.b. testResource ist, können Sie testResource angeben.</span><span class="sxs-lookup"><span data-stu-id="613a0-155">e.g. if your resource name is testResource, you can specify testResource.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="613a0-156">-</span><span class="sxs-lookup"><span data-stu-id="613a0-156">-ResourceType</span></span>
<span data-ttu-id="613a0-157">Gibt den Typ einer Ressource an.</span><span class="sxs-lookup"><span data-stu-id="613a0-157">Specifies the type of a resource.</span></span>
<span data-ttu-id="613a0-158">Bei einer Datenbank lautet der Ressourcentyp beispielsweise wie folgt:</span><span class="sxs-lookup"><span data-stu-id="613a0-158">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

<span data-ttu-id="613a0-159">Dieses Cmdlet sucht nach Ressourcen des angegebenen Typs.</span><span class="sxs-lookup"><span data-stu-id="613a0-159">This cmdlet searches for resources of the specified type.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="613a0-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="613a0-160">-Tag</span></span>
<span data-ttu-id="613a0-161">Der Transponder Filter für die OData-Abfrage.</span><span class="sxs-lookup"><span data-stu-id="613a0-161">The tag filter for the OData query.</span></span> <span data-ttu-id="613a0-162">Das erwartete Format ist @ {Tagname = $NULL} oder @ {Tagname = ' tagValue '}.</span><span class="sxs-lookup"><span data-stu-id="613a0-162">The expected format is @{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: Hashtable
Parameter Sets: GetByTagObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="613a0-163">-Tagname</span><span class="sxs-lookup"><span data-stu-id="613a0-163">-TagName</span></span>
```yaml
Type: String
Parameter Sets: GetByTagNameValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="613a0-164">-TagValue</span><span class="sxs-lookup"><span data-stu-id="613a0-164">-TagValue</span></span>
```yaml
Type: String
Parameter Sets: GetByTagNameValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="613a0-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="613a0-165">-TenantLevel</span></span>
<span data-ttu-id="613a0-166">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="613a0-166">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="613a0-167">-Top</span><span class="sxs-lookup"><span data-stu-id="613a0-167">-Top</span></span>
<span data-ttu-id="613a0-168">Gibt die Anzahl der Ressourcen an, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="613a0-168">Specifies the number of resources to retrieve.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="613a0-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="613a0-169">CommonParameters</span></span>
<span data-ttu-id="613a0-170">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="613a0-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="613a0-171">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="613a0-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="613a0-172">Eingaben</span><span class="sxs-lookup"><span data-stu-id="613a0-172">INPUTS</span></span>

### <span data-ttu-id="613a0-173">Keine</span><span class="sxs-lookup"><span data-stu-id="613a0-173">None</span></span>
<span data-ttu-id="613a0-174">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="613a0-174">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="613a0-175">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="613a0-175">OUTPUTS</span></span>

### <span data-ttu-id="613a0-176">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="613a0-176">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="613a0-177">Notizen</span><span class="sxs-lookup"><span data-stu-id="613a0-177">NOTES</span></span>

## <span data-ttu-id="613a0-178">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="613a0-178">RELATED LINKS</span></span>

[<span data-ttu-id="613a0-179">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="613a0-179">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="613a0-180">Verschieben-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="613a0-180">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="613a0-181">Neu – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="613a0-181">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="613a0-182">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="613a0-182">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="613a0-183">Satz-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="613a0-183">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
