---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 125e349fd2644fcfcd4cf2b6758fe45c40f323b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948995"
---
# <span data-ttu-id="ea49a-101">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ea49a-101">Set-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="ea49a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea49a-102">SYNOPSIS</span></span>
<span data-ttu-id="ea49a-103">Aktualisiert einen API-Versionssatz im API-Verwaltungskontext.</span><span class="sxs-lookup"><span data-stu-id="ea49a-103">Updates an API Version Set in the API Management Context.</span></span>

## <span data-ttu-id="ea49a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea49a-104">SYNTAX</span></span>

### <span data-ttu-id="ea49a-105">ExpandedParameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="ea49a-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea49a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ea49a-106">ByInputObject</span></span>
```
Set-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea49a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea49a-107">DESCRIPTION</span></span>

<span data-ttu-id="ea49a-108">Das **Cmdlet Set-AzApiManagementApiVersionSet** ändert einen Azure API Management API-Versionssatz.</span><span class="sxs-lookup"><span data-stu-id="ea49a-108">The **Set-AzApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="ea49a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ea49a-109">EXAMPLES</span></span>

### <span data-ttu-id="ea49a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ea49a-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="ea49a-111">Mit diesem Befehl wird ein vorhandener API-Versionssatz mit dem Versionsschema und `Header` dem Headerparameter `api-version` aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ea49a-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="ea49a-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ea49a-112">PARAMETERS</span></span>

### <span data-ttu-id="ea49a-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="ea49a-113">-ApiVersionSetId</span></span>
<span data-ttu-id="ea49a-114">Bezeichner für den neuen API-Versionssatz.</span><span class="sxs-lookup"><span data-stu-id="ea49a-114">Identifier for new API Version Set.</span></span>

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

### <span data-ttu-id="ea49a-115">-Context</span><span class="sxs-lookup"><span data-stu-id="ea49a-115">-Context</span></span>
<span data-ttu-id="ea49a-116">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ea49a-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ea49a-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ea49a-117">This parameter is required.</span></span>

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

### <span data-ttu-id="ea49a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea49a-118">-DefaultProfile</span></span>
<span data-ttu-id="ea49a-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea49a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea49a-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ea49a-120">-Description</span></span>
<span data-ttu-id="ea49a-121">Beschreibung des Api-Versionssets.</span><span class="sxs-lookup"><span data-stu-id="ea49a-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="ea49a-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="ea49a-122">-HeaderName</span></span>
<span data-ttu-id="ea49a-123">Der Wert "Header", der die Versionsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="ea49a-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="ea49a-124">Wenn Versionsschemaheader ausgewählt ist, muss dieser Wert angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ea49a-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="ea49a-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea49a-125">-InputObject</span></span>
<span data-ttu-id="ea49a-126">Instanz von PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="ea49a-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="ea49a-127">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ea49a-127">This parameter is required.</span></span>

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

### <span data-ttu-id="ea49a-128">-Name</span><span class="sxs-lookup"><span data-stu-id="ea49a-128">-Name</span></span>
<span data-ttu-id="ea49a-129">Der Name des ApiVersionssets.</span><span class="sxs-lookup"><span data-stu-id="ea49a-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="ea49a-130">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="ea49a-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="ea49a-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea49a-131">-PassThru</span></span>
<span data-ttu-id="ea49a-132">Wenn angegeben, wird die Instanz des Typs Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet, der den geänderten apiVersionSet darstellt, in die Ausgabe geschrieben.</span><span class="sxs-lookup"><span data-stu-id="ea49a-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

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

### <span data-ttu-id="ea49a-133">-QueryName</span><span class="sxs-lookup"><span data-stu-id="ea49a-133">-QueryName</span></span>
<span data-ttu-id="ea49a-134">Der Abfragewert, der die Versionsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="ea49a-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="ea49a-135">Wenn Die Versionsschemaabfrage ausgewählt ist, muss dieser Wert angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ea49a-135">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="ea49a-136">-Schema</span><span class="sxs-lookup"><span data-stu-id="ea49a-136">-Scheme</span></span>
<span data-ttu-id="ea49a-137">Versionsschema zum Auswählen für den Api-Versionssatz.</span><span class="sxs-lookup"><span data-stu-id="ea49a-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="ea49a-138">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="ea49a-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="ea49a-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ea49a-139">-Confirm</span></span>
<span data-ttu-id="ea49a-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ea49a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea49a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea49a-141">-WhatIf</span></span>
<span data-ttu-id="ea49a-142">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ea49a-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea49a-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ea49a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea49a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea49a-144">CommonParameters</span></span>
<span data-ttu-id="ea49a-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea49a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea49a-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea49a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea49a-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ea49a-147">INPUTS</span></span>

### <span data-ttu-id="ea49a-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ea49a-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ea49a-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ea49a-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="ea49a-150">System.String</span><span class="sxs-lookup"><span data-stu-id="ea49a-150">System.String</span></span>

### <span data-ttu-id="ea49a-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="ea49a-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="ea49a-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ea49a-152">OUTPUTS</span></span>

### <span data-ttu-id="ea49a-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ea49a-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="ea49a-154">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ea49a-154">NOTES</span></span>

## <span data-ttu-id="ea49a-155">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ea49a-155">RELATED LINKS</span></span>

[<span data-ttu-id="ea49a-156">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ea49a-156">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="ea49a-157">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ea49a-157">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="ea49a-158">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ea49a-158">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
