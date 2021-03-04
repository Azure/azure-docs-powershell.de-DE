---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: b8eac81d90f20617399048464ecca40e0df8d93f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925371"
---
# <span data-ttu-id="214f6-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="214f6-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="214f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="214f6-102">SYNOPSIS</span></span>
<span data-ttu-id="214f6-103">Ändert eine API-Überarbeitung</span><span class="sxs-lookup"><span data-stu-id="214f6-103">Modifies an API Revision</span></span>

## <span data-ttu-id="214f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="214f6-104">SYNTAX</span></span>

### <span data-ttu-id="214f6-105">ExpandedParameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="214f6-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 [-Name <String>] [-Description <String>] [-ServiceUrl <String>] [-Path <String>]
 [-Protocols <PsApiManagementSchema[]>] [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-OpenIdProviderId <String>] [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="214f6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="214f6-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="214f6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="214f6-107">DESCRIPTION</span></span>
<span data-ttu-id="214f6-108">Das **Cmdlet Set-AzApiManagementApiRevision** ändert eine Azure API Management API Revision.</span><span class="sxs-lookup"><span data-stu-id="214f6-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="214f6-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="214f6-109">EXAMPLES</span></span>

### <span data-ttu-id="214f6-110">Beispiel 1: Ändern einer API-Überarbeitung</span><span class="sxs-lookup"><span data-stu-id="214f6-110">Example 1: Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="214f6-111">Das Cmdlet aktualisiert die `2` Überarbeitung der API mit einer neuen `echo-api` Beschreibung, einem neuen Protokoll und einem neuen Pfad.</span><span class="sxs-lookup"><span data-stu-id="214f6-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="214f6-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="214f6-112">PARAMETERS</span></span>

### <span data-ttu-id="214f6-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="214f6-113">-ApiId</span></span>
<span data-ttu-id="214f6-114">Bezeichner der vorhandenen API.</span><span class="sxs-lookup"><span data-stu-id="214f6-114">Identifier of existing API.</span></span>
<span data-ttu-id="214f6-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="214f6-115">This parameter is required.</span></span>

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

### <span data-ttu-id="214f6-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="214f6-116">-ApiRevision</span></span>
<span data-ttu-id="214f6-117">Bezeichner der vorhandenen API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="214f6-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="214f6-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="214f6-118">This parameter is required.</span></span>

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

### <span data-ttu-id="214f6-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="214f6-119">-AuthorizationScope</span></span>
<span data-ttu-id="214f6-120">OAuth-Operationsbereich.</span><span class="sxs-lookup"><span data-stu-id="214f6-120">OAuth operations scope.</span></span>
<span data-ttu-id="214f6-121">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="214f6-121">This parameter is optional.</span></span>
<span data-ttu-id="214f6-122">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="214f6-122">Default value is $null.</span></span>

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

### <span data-ttu-id="214f6-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="214f6-123">-AuthorizationServerId</span></span>
<span data-ttu-id="214f6-124">OAuth Authorization Server Identifier.</span><span class="sxs-lookup"><span data-stu-id="214f6-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="214f6-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="214f6-125">This parameter is optional.</span></span>
<span data-ttu-id="214f6-126">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="214f6-126">Default value is $null.</span></span>
<span data-ttu-id="214f6-127">Muss angegeben werden, wenn AuthorizationScope angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="214f6-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="214f6-128">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="214f6-128">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="214f6-129">OpenId-Autorisierungsservermechanismus, über den das Zugriffstoken an die API übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="214f6-129">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="214f6-130">Weitere Informationen finden Sie unter http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="214f6-130">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="214f6-131">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="214f6-131">This parameter is optional.</span></span> <span data-ttu-id="214f6-132">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="214f6-132">Default value is $null.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="214f6-133">-Context</span><span class="sxs-lookup"><span data-stu-id="214f6-133">-Context</span></span>
<span data-ttu-id="214f6-134">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="214f6-134">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="214f6-135">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="214f6-135">This parameter is required.</span></span>

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

### <span data-ttu-id="214f6-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="214f6-136">-DefaultProfile</span></span>
<span data-ttu-id="214f6-137">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="214f6-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="214f6-138">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="214f6-138">-Description</span></span>
<span data-ttu-id="214f6-139">Web-API-Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="214f6-139">Web API description.</span></span>
<span data-ttu-id="214f6-140">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="214f6-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="214f6-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="214f6-141">-InputObject</span></span>
<span data-ttu-id="214f6-142">Instanz von PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="214f6-142">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="214f6-143">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="214f6-143">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="214f6-144">-Name</span><span class="sxs-lookup"><span data-stu-id="214f6-144">-Name</span></span>
<span data-ttu-id="214f6-145">Web-API-Name.</span><span class="sxs-lookup"><span data-stu-id="214f6-145">Web API name.</span></span>
<span data-ttu-id="214f6-146">Öffentlicher Name der API, wie sie auf den Entwickler- und Administratorportalen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="214f6-146">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="214f6-147">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="214f6-147">This parameter is required.</span></span>

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

### <span data-ttu-id="214f6-148">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="214f6-148">-OpenIdProviderId</span></span>
<span data-ttu-id="214f6-149">OpenId Authorization Server Identifier.</span><span class="sxs-lookup"><span data-stu-id="214f6-149">OpenId authorization server identifier.</span></span> <span data-ttu-id="214f6-150">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="214f6-150">This parameter is optional.</span></span> <span data-ttu-id="214f6-151">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="214f6-151">Default value is $null.</span></span> <span data-ttu-id="214f6-152">Muss angegeben werden, wenn BearerTokenSendingMethods angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="214f6-152">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="214f6-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="214f6-153">-PassThru</span></span>
<span data-ttu-id="214f6-154">Wenn angegeben, wird die Instanz des Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi-Typs angegeben, der die festgelegte API darstellt.</span><span class="sxs-lookup"><span data-stu-id="214f6-154">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="214f6-155">-Path</span><span class="sxs-lookup"><span data-stu-id="214f6-155">-Path</span></span>
<span data-ttu-id="214f6-156">Web-API-Pfad.</span><span class="sxs-lookup"><span data-stu-id="214f6-156">Web API Path.</span></span>
<span data-ttu-id="214f6-157">Letzter Teil der öffentlichen URL der API.</span><span class="sxs-lookup"><span data-stu-id="214f6-157">Last part of the API's public URL.</span></span>
<span data-ttu-id="214f6-158">Diese URL wird von API-Konsumenten zum Senden von Anforderungen an den Webdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="214f6-158">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="214f6-159">Muss 1 bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="214f6-159">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="214f6-160">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="214f6-160">This parameter is optional.</span></span>
<span data-ttu-id="214f6-161">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="214f6-161">Default value is $null.</span></span>

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

### <span data-ttu-id="214f6-162">-Protokolle</span><span class="sxs-lookup"><span data-stu-id="214f6-162">-Protocols</span></span>
<span data-ttu-id="214f6-163">Web-API-Protokolle (http, https).</span><span class="sxs-lookup"><span data-stu-id="214f6-163">Web API protocols (http, https).</span></span>
<span data-ttu-id="214f6-164">Protokolle, über die API verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="214f6-164">Protocols over which API is made available.</span></span>
<span data-ttu-id="214f6-165">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="214f6-165">This parameter is required.</span></span>
<span data-ttu-id="214f6-166">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="214f6-166">Default value is $null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="214f6-167">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="214f6-167">-ServiceUrl</span></span>
<span data-ttu-id="214f6-168">Eine URL des Webdiensts, der die API verfügbar machen soll.</span><span class="sxs-lookup"><span data-stu-id="214f6-168">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="214f6-169">Diese URL wird nur von Azure API Management verwendet und nicht öffentlich gemacht.</span><span class="sxs-lookup"><span data-stu-id="214f6-169">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="214f6-170">Muss 1 bis 2000 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="214f6-170">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="214f6-171">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="214f6-171">This parameter is required.</span></span>

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

### <span data-ttu-id="214f6-172">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="214f6-172">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="214f6-173">Name des Abonnementschlüssels.</span><span class="sxs-lookup"><span data-stu-id="214f6-173">Subscription key header name.</span></span>
<span data-ttu-id="214f6-174">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="214f6-174">This parameter is optional.</span></span>
<span data-ttu-id="214f6-175">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="214f6-175">Default value is $null.</span></span>

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

### <span data-ttu-id="214f6-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="214f6-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="214f6-177">Parametername der Abonnementschlüsselabfragezeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="214f6-177">Subscription key query string parameter name.</span></span>
<span data-ttu-id="214f6-178">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="214f6-178">This parameter is optional.</span></span>
<span data-ttu-id="214f6-179">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="214f6-179">Default value is $null.</span></span>

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

### <span data-ttu-id="214f6-180">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="214f6-180">-SubscriptionRequired</span></span>
<span data-ttu-id="214f6-181">Kennzeichnen, um SubscriptionRequired für Anforderungen an die Api zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="214f6-181">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="214f6-182">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="214f6-182">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="214f6-183">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="214f6-183">-Confirm</span></span>
<span data-ttu-id="214f6-184">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="214f6-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="214f6-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="214f6-185">-WhatIf</span></span>
<span data-ttu-id="214f6-186">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="214f6-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="214f6-187">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="214f6-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="214f6-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="214f6-188">CommonParameters</span></span>
<span data-ttu-id="214f6-189">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="214f6-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="214f6-190">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="214f6-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="214f6-191">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="214f6-191">INPUTS</span></span>

### <span data-ttu-id="214f6-192">System.String</span><span class="sxs-lookup"><span data-stu-id="214f6-192">System.String</span></span>

### <span data-ttu-id="214f6-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="214f6-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="214f6-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="214f6-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="214f6-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span><span class="sxs-lookup"><span data-stu-id="214f6-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="214f6-196">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="214f6-196">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="214f6-197">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="214f6-197">OUTPUTS</span></span>

### <span data-ttu-id="214f6-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="214f6-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="214f6-199">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="214f6-199">NOTES</span></span>

## <span data-ttu-id="214f6-200">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="214f6-200">RELATED LINKS</span></span>

[<span data-ttu-id="214f6-201">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="214f6-201">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="214f6-202">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="214f6-202">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="214f6-203">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="214f6-203">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)