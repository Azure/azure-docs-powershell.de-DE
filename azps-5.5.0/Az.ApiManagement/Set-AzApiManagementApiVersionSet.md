---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
ms.openlocfilehash: d85d480adc5d6c588c7da2f03c514258dc96a9e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171773"
---
# <span data-ttu-id="37503-101">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="37503-101">Set-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="37503-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37503-102">SYNOPSIS</span></span>
<span data-ttu-id="37503-103">Aktualisiert einen API-Versionssatz im API-Verwaltungskontext.</span><span class="sxs-lookup"><span data-stu-id="37503-103">Updates an API Version Set in the API Management Context.</span></span>

## <span data-ttu-id="37503-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37503-104">SYNTAX</span></span>

### <span data-ttu-id="37503-105">ExpandedParameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="37503-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37503-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="37503-106">ByInputObject</span></span>
```
Set-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="37503-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37503-107">DESCRIPTION</span></span>

<span data-ttu-id="37503-108">Das **Cmdlet "Set-AzApiManagementApiVersionSet"** ändert den Versionssatz einer Azure API Management API.</span><span class="sxs-lookup"><span data-stu-id="37503-108">The **Set-AzApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="37503-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="37503-109">EXAMPLES</span></span>

### <span data-ttu-id="37503-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="37503-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="37503-111">Mit diesem Befehl wird ein vorhandener API-Versionssatz mit dem Versionsschema und `Header` dem Headerparameter `api-version` aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="37503-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="37503-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37503-112">PARAMETERS</span></span>

### <span data-ttu-id="37503-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="37503-113">-ApiVersionSetId</span></span>
<span data-ttu-id="37503-114">Id für neue API-Versionssatz.</span><span class="sxs-lookup"><span data-stu-id="37503-114">Identifier for new API Version Set.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37503-115">-Context</span><span class="sxs-lookup"><span data-stu-id="37503-115">-Context</span></span>
<span data-ttu-id="37503-116">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="37503-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="37503-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="37503-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37503-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37503-118">-DefaultProfile</span></span>
<span data-ttu-id="37503-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37503-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37503-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37503-120">-Description</span></span>
<span data-ttu-id="37503-121">Beschreibung des Api-Versions-Sets.</span><span class="sxs-lookup"><span data-stu-id="37503-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="37503-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="37503-122">-HeaderName</span></span>
<span data-ttu-id="37503-123">Der Headerwert, der die Versionsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="37503-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="37503-124">Wenn schema header für die Versionsversion ausgewählt wird, muss dieser Wert angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="37503-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="37503-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37503-125">-InputObject</span></span>
<span data-ttu-id="37503-126">Instanz von PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="37503-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="37503-127">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="37503-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37503-128">-Name</span><span class="sxs-lookup"><span data-stu-id="37503-128">-Name</span></span>
<span data-ttu-id="37503-129">Der Name des ApiVersion-Sets.</span><span class="sxs-lookup"><span data-stu-id="37503-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="37503-130">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="37503-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="37503-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37503-131">-PassThru</span></span>
<span data-ttu-id="37503-132">Wenn angegeben, wird eine Instanz des Typs "Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet", der den geänderten "apiVersionSet"-Typ darstellt, in die Ausgabe geschrieben.</span><span class="sxs-lookup"><span data-stu-id="37503-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

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

### <span data-ttu-id="37503-133">-QueryName</span><span class="sxs-lookup"><span data-stu-id="37503-133">-QueryName</span></span>
<span data-ttu-id="37503-134">Der Abfragewert, der die Versionsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="37503-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="37503-135">Wenn eine Schemaabfrage für die Versionsierung ausgewählt wird, muss dieser Wert angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="37503-135">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="37503-136">-Schema</span><span class="sxs-lookup"><span data-stu-id="37503-136">-Scheme</span></span>
<span data-ttu-id="37503-137">Versionsschema zum Auswählen für den API-Versionssatz.</span><span class="sxs-lookup"><span data-stu-id="37503-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="37503-138">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="37503-138">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37503-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37503-139">-Confirm</span></span>
<span data-ttu-id="37503-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="37503-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37503-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="37503-141">-WhatIf</span></span>
<span data-ttu-id="37503-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37503-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37503-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37503-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37503-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37503-144">CommonParameters</span></span>
<span data-ttu-id="37503-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37503-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37503-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37503-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37503-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="37503-147">INPUTS</span></span>

### <span data-ttu-id="37503-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="37503-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="37503-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="37503-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="37503-150">System.String</span><span class="sxs-lookup"><span data-stu-id="37503-150">System.String</span></span>

### <span data-ttu-id="37503-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="37503-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="37503-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="37503-152">OUTPUTS</span></span>

### <span data-ttu-id="37503-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="37503-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="37503-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="37503-154">NOTES</span></span>

## <span data-ttu-id="37503-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="37503-155">RELATED LINKS</span></span>

[<span data-ttu-id="37503-156">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="37503-156">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="37503-157">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="37503-157">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="37503-158">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="37503-158">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
