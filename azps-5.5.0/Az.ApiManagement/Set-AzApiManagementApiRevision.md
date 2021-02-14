---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: fcae55c69b1874e06ce9110631baaf3b679fe99a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176244"
---
# <span data-ttu-id="513ff-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="513ff-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="513ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="513ff-102">SYNOPSIS</span></span>
<span data-ttu-id="513ff-103">Ändert eine API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="513ff-103">Modifies an API Revision</span></span>

## <span data-ttu-id="513ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="513ff-104">SYNTAX</span></span>

### <span data-ttu-id="513ff-105">ExpandedParameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="513ff-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 [-Name <String>] [-Description <String>] [-ServiceUrl <String>] [-Path <String>]
 [-Protocols <PsApiManagementSchema[]>] [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-OpenIdProviderId <String>] [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="513ff-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="513ff-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="513ff-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="513ff-107">DESCRIPTION</span></span>
<span data-ttu-id="513ff-108">Das **Cmdlet "Set-AzApiManagementApiRevision"** ändert eine Überarbeitung der Azure API Management API.</span><span class="sxs-lookup"><span data-stu-id="513ff-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="513ff-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="513ff-109">EXAMPLES</span></span>

### <span data-ttu-id="513ff-110">Beispiel 1: Ändern einer API-Überarbeitung</span><span class="sxs-lookup"><span data-stu-id="513ff-110">Example 1: Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="513ff-111">Das Cmdlet aktualisiert die Überarbeitung der API mit einer neuen `2` `echo-api` Beschreibung, einem neuen Protokoll und einem neuen Pfad.</span><span class="sxs-lookup"><span data-stu-id="513ff-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="513ff-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="513ff-112">PARAMETERS</span></span>

### <span data-ttu-id="513ff-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="513ff-113">-ApiId</span></span>
<span data-ttu-id="513ff-114">Bezeichner einer vorhandenen API.</span><span class="sxs-lookup"><span data-stu-id="513ff-114">Identifier of existing API.</span></span>
<span data-ttu-id="513ff-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="513ff-115">This parameter is required.</span></span>

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

### <span data-ttu-id="513ff-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="513ff-116">-ApiRevision</span></span>
<span data-ttu-id="513ff-117">Bezeichner einer vorhandenen API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="513ff-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="513ff-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="513ff-118">This parameter is required.</span></span>

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

### <span data-ttu-id="513ff-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="513ff-119">-AuthorizationScope</span></span>
<span data-ttu-id="513ff-120">Bereich der OAuth-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="513ff-120">OAuth operations scope.</span></span>
<span data-ttu-id="513ff-121">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="513ff-121">This parameter is optional.</span></span>
<span data-ttu-id="513ff-122">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="513ff-122">Default value is $null.</span></span>

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

### <span data-ttu-id="513ff-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="513ff-123">-AuthorizationServerId</span></span>
<span data-ttu-id="513ff-124">Id des OAuth-Autorisierungsservers.</span><span class="sxs-lookup"><span data-stu-id="513ff-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="513ff-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="513ff-125">This parameter is optional.</span></span>
<span data-ttu-id="513ff-126">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="513ff-126">Default value is $null.</span></span>
<span data-ttu-id="513ff-127">Muss angegeben werden, wenn AuthorizationScope angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="513ff-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="513ff-128">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="513ff-128">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="513ff-129">OpenId authorization server mechanism by which access token is passed to the API.</span><span class="sxs-lookup"><span data-stu-id="513ff-129">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="513ff-130">Weitere Informationen finden Sie unter http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="513ff-130">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="513ff-131">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="513ff-131">This parameter is optional.</span></span> <span data-ttu-id="513ff-132">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="513ff-132">Default value is $null.</span></span>

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

### <span data-ttu-id="513ff-133">-Context</span><span class="sxs-lookup"><span data-stu-id="513ff-133">-Context</span></span>
<span data-ttu-id="513ff-134">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="513ff-134">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="513ff-135">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="513ff-135">This parameter is required.</span></span>

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

### <span data-ttu-id="513ff-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="513ff-136">-DefaultProfile</span></span>
<span data-ttu-id="513ff-137">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="513ff-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="513ff-138">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="513ff-138">-Description</span></span>
<span data-ttu-id="513ff-139">Web-API-Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="513ff-139">Web API description.</span></span>
<span data-ttu-id="513ff-140">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="513ff-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="513ff-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="513ff-141">-InputObject</span></span>
<span data-ttu-id="513ff-142">Instanz von PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="513ff-142">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="513ff-143">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="513ff-143">This parameter is required.</span></span>

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

### <span data-ttu-id="513ff-144">-Name</span><span class="sxs-lookup"><span data-stu-id="513ff-144">-Name</span></span>
<span data-ttu-id="513ff-145">Web-API-Name.</span><span class="sxs-lookup"><span data-stu-id="513ff-145">Web API name.</span></span>
<span data-ttu-id="513ff-146">Öffentlicher Name der API, wie er auf den Entwickler- und Administratorportalen angezeigt würde.</span><span class="sxs-lookup"><span data-stu-id="513ff-146">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="513ff-147">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="513ff-147">This parameter is required.</span></span>

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

### <span data-ttu-id="513ff-148">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="513ff-148">-OpenIdProviderId</span></span>
<span data-ttu-id="513ff-149">OpenId-Autorisierungsserver-ID.</span><span class="sxs-lookup"><span data-stu-id="513ff-149">OpenId authorization server identifier.</span></span> <span data-ttu-id="513ff-150">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="513ff-150">This parameter is optional.</span></span> <span data-ttu-id="513ff-151">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="513ff-151">Default value is $null.</span></span> <span data-ttu-id="513ff-152">Muss angegeben werden, wenn BearerTokenSendingMethods angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="513ff-152">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="513ff-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="513ff-153">-PassThru</span></span>
<span data-ttu-id="513ff-154">Wenn angegeben, dann Instanz des Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi-Typs, der die festgelegte API darstellt.</span><span class="sxs-lookup"><span data-stu-id="513ff-154">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="513ff-155">-Path</span><span class="sxs-lookup"><span data-stu-id="513ff-155">-Path</span></span>
<span data-ttu-id="513ff-156">Web-API-Pfad.</span><span class="sxs-lookup"><span data-stu-id="513ff-156">Web API Path.</span></span>
<span data-ttu-id="513ff-157">Letzter Teil der öffentlichen URL der API.</span><span class="sxs-lookup"><span data-stu-id="513ff-157">Last part of the API's public URL.</span></span>
<span data-ttu-id="513ff-158">Diese URL wird von API-Kunden verwendet, um Anforderungen an den Webdienst zu senden.</span><span class="sxs-lookup"><span data-stu-id="513ff-158">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="513ff-159">Muss 1 bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="513ff-159">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="513ff-160">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="513ff-160">This parameter is optional.</span></span>
<span data-ttu-id="513ff-161">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="513ff-161">Default value is $null.</span></span>

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

### <span data-ttu-id="513ff-162">-Protocols</span><span class="sxs-lookup"><span data-stu-id="513ff-162">-Protocols</span></span>
<span data-ttu-id="513ff-163">Web-API-Protokolle (http, https).</span><span class="sxs-lookup"><span data-stu-id="513ff-163">Web API protocols (http, https).</span></span>
<span data-ttu-id="513ff-164">Protokolle, über die API verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="513ff-164">Protocols over which API is made available.</span></span>
<span data-ttu-id="513ff-165">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="513ff-165">This parameter is required.</span></span>
<span data-ttu-id="513ff-166">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="513ff-166">Default value is $null.</span></span>

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

### <span data-ttu-id="513ff-167">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="513ff-167">-ServiceUrl</span></span>
<span data-ttu-id="513ff-168">Eine URL des Webdiensts, der die API verfügbar machen soll.</span><span class="sxs-lookup"><span data-stu-id="513ff-168">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="513ff-169">Diese URL wird nur von Azure API Management verwendet und nicht öffentlich gemacht.</span><span class="sxs-lookup"><span data-stu-id="513ff-169">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="513ff-170">Muss 1 bis 2.000 Zeichen umfassen.</span><span class="sxs-lookup"><span data-stu-id="513ff-170">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="513ff-171">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="513ff-171">This parameter is required.</span></span>

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

### <span data-ttu-id="513ff-172">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="513ff-172">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="513ff-173">Name der Kopfzeile des Abonnementschlüssels.</span><span class="sxs-lookup"><span data-stu-id="513ff-173">Subscription key header name.</span></span>
<span data-ttu-id="513ff-174">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="513ff-174">This parameter is optional.</span></span>
<span data-ttu-id="513ff-175">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="513ff-175">Default value is $null.</span></span>

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

### <span data-ttu-id="513ff-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="513ff-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="513ff-177">Parametername der Abonnementschlüsselabfragezeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="513ff-177">Subscription key query string parameter name.</span></span>
<span data-ttu-id="513ff-178">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="513ff-178">This parameter is optional.</span></span>
<span data-ttu-id="513ff-179">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="513ff-179">Default value is $null.</span></span>

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

### <span data-ttu-id="513ff-180">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="513ff-180">-SubscriptionRequired</span></span>
<span data-ttu-id="513ff-181">Flag zum Erzwingen von "SubscriptionRequired" für Anforderungen an die API.</span><span class="sxs-lookup"><span data-stu-id="513ff-181">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="513ff-182">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="513ff-182">This parameter is optional.</span></span>

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

### <span data-ttu-id="513ff-183">-Confirm</span><span class="sxs-lookup"><span data-stu-id="513ff-183">-Confirm</span></span>
<span data-ttu-id="513ff-184">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="513ff-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="513ff-185">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="513ff-185">-WhatIf</span></span>
<span data-ttu-id="513ff-186">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="513ff-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="513ff-187">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="513ff-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="513ff-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="513ff-188">CommonParameters</span></span>
<span data-ttu-id="513ff-189">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="513ff-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="513ff-190">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="513ff-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="513ff-191">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="513ff-191">INPUTS</span></span>

### <span data-ttu-id="513ff-192">System.String</span><span class="sxs-lookup"><span data-stu-id="513ff-192">System.String</span></span>

### <span data-ttu-id="513ff-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="513ff-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="513ff-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="513ff-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="513ff-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span><span class="sxs-lookup"><span data-stu-id="513ff-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="513ff-196">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="513ff-196">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="513ff-197">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="513ff-197">OUTPUTS</span></span>

### <span data-ttu-id="513ff-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="513ff-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="513ff-199">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="513ff-199">NOTES</span></span>

## <span data-ttu-id="513ff-200">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="513ff-200">RELATED LINKS</span></span>

[<span data-ttu-id="513ff-201">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="513ff-201">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="513ff-202">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="513ff-202">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="513ff-203">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="513ff-203">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)