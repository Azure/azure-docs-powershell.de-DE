---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: fcae55c69b1874e06ce9110631baaf3b679fe99a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381841"
---
# <span data-ttu-id="47193-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="47193-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="47193-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47193-102">SYNOPSIS</span></span>
<span data-ttu-id="47193-103">Ändert eine API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="47193-103">Modifies an API Revision</span></span>

## <span data-ttu-id="47193-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47193-104">SYNTAX</span></span>

### <span data-ttu-id="47193-105">ExpandedParameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="47193-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 [-Name <String>] [-Description <String>] [-ServiceUrl <String>] [-Path <String>]
 [-Protocols <PsApiManagementSchema[]>] [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-OpenIdProviderId <String>] [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47193-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="47193-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47193-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47193-107">DESCRIPTION</span></span>
<span data-ttu-id="47193-108">Das **Cmdlet "Set-AzApiManagementApiRevision"** ändert eine Überarbeitung der Azure API Management API.</span><span class="sxs-lookup"><span data-stu-id="47193-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="47193-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="47193-109">EXAMPLES</span></span>

### <span data-ttu-id="47193-110">Beispiel 1: Ändern einer API-Überarbeitung</span><span class="sxs-lookup"><span data-stu-id="47193-110">Example 1: Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="47193-111">Das Cmdlet aktualisiert die Überarbeitung der API mit einer neuen `2` `echo-api` Beschreibung, einem neuen Protokoll und einem neuen Pfad.</span><span class="sxs-lookup"><span data-stu-id="47193-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="47193-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47193-112">PARAMETERS</span></span>

### <span data-ttu-id="47193-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="47193-113">-ApiId</span></span>
<span data-ttu-id="47193-114">Bezeichner einer vorhandenen API.</span><span class="sxs-lookup"><span data-stu-id="47193-114">Identifier of existing API.</span></span>
<span data-ttu-id="47193-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="47193-115">This parameter is required.</span></span>

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

### <span data-ttu-id="47193-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="47193-116">-ApiRevision</span></span>
<span data-ttu-id="47193-117">Bezeichner einer vorhandenen API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="47193-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="47193-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="47193-118">This parameter is required.</span></span>

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

### <span data-ttu-id="47193-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="47193-119">-AuthorizationScope</span></span>
<span data-ttu-id="47193-120">Bereich der OAuth-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="47193-120">OAuth operations scope.</span></span>
<span data-ttu-id="47193-121">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="47193-121">This parameter is optional.</span></span>
<span data-ttu-id="47193-122">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="47193-122">Default value is $null.</span></span>

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

### <span data-ttu-id="47193-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="47193-123">-AuthorizationServerId</span></span>
<span data-ttu-id="47193-124">Id des OAuth-Autorisierungsservers.</span><span class="sxs-lookup"><span data-stu-id="47193-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="47193-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="47193-125">This parameter is optional.</span></span>
<span data-ttu-id="47193-126">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="47193-126">Default value is $null.</span></span>
<span data-ttu-id="47193-127">Muss angegeben werden, wenn AuthorizationScope angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="47193-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="47193-128">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="47193-128">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="47193-129">OpenId authorization server mechanism by which access token is passed to the API.</span><span class="sxs-lookup"><span data-stu-id="47193-129">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="47193-130">Weitere Informationen finden Sie unter http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="47193-130">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="47193-131">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="47193-131">This parameter is optional.</span></span> <span data-ttu-id="47193-132">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="47193-132">Default value is $null.</span></span>

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

### <span data-ttu-id="47193-133">-Context</span><span class="sxs-lookup"><span data-stu-id="47193-133">-Context</span></span>
<span data-ttu-id="47193-134">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="47193-134">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="47193-135">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="47193-135">This parameter is required.</span></span>

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

### <span data-ttu-id="47193-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47193-136">-DefaultProfile</span></span>
<span data-ttu-id="47193-137">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47193-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47193-138">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47193-138">-Description</span></span>
<span data-ttu-id="47193-139">Web-API-Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="47193-139">Web API description.</span></span>
<span data-ttu-id="47193-140">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="47193-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="47193-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47193-141">-InputObject</span></span>
<span data-ttu-id="47193-142">Instanz von PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="47193-142">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="47193-143">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="47193-143">This parameter is required.</span></span>

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

### <span data-ttu-id="47193-144">-Name</span><span class="sxs-lookup"><span data-stu-id="47193-144">-Name</span></span>
<span data-ttu-id="47193-145">Web-API-Name.</span><span class="sxs-lookup"><span data-stu-id="47193-145">Web API name.</span></span>
<span data-ttu-id="47193-146">Öffentlicher Name der API, wie er auf den Entwickler- und Administratorportalen angezeigt würde.</span><span class="sxs-lookup"><span data-stu-id="47193-146">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="47193-147">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="47193-147">This parameter is required.</span></span>

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

### <span data-ttu-id="47193-148">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="47193-148">-OpenIdProviderId</span></span>
<span data-ttu-id="47193-149">OpenId-Autorisierungsserver-ID.</span><span class="sxs-lookup"><span data-stu-id="47193-149">OpenId authorization server identifier.</span></span> <span data-ttu-id="47193-150">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="47193-150">This parameter is optional.</span></span> <span data-ttu-id="47193-151">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="47193-151">Default value is $null.</span></span> <span data-ttu-id="47193-152">Muss angegeben werden, wenn BearerTokenSendingMethods angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="47193-152">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="47193-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47193-153">-PassThru</span></span>
<span data-ttu-id="47193-154">Wenn angegeben, dann Instanz des Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi-Typs, der die festgelegte API darstellt.</span><span class="sxs-lookup"><span data-stu-id="47193-154">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="47193-155">-Path</span><span class="sxs-lookup"><span data-stu-id="47193-155">-Path</span></span>
<span data-ttu-id="47193-156">Web-API-Pfad.</span><span class="sxs-lookup"><span data-stu-id="47193-156">Web API Path.</span></span>
<span data-ttu-id="47193-157">Letzter Teil der öffentlichen URL der API.</span><span class="sxs-lookup"><span data-stu-id="47193-157">Last part of the API's public URL.</span></span>
<span data-ttu-id="47193-158">Diese URL wird von API-Kunden verwendet, um Anforderungen an den Webdienst zu senden.</span><span class="sxs-lookup"><span data-stu-id="47193-158">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="47193-159">Muss 1 bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="47193-159">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="47193-160">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="47193-160">This parameter is optional.</span></span>
<span data-ttu-id="47193-161">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="47193-161">Default value is $null.</span></span>

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

### <span data-ttu-id="47193-162">-Protocols</span><span class="sxs-lookup"><span data-stu-id="47193-162">-Protocols</span></span>
<span data-ttu-id="47193-163">Web-API-Protokolle (http, https).</span><span class="sxs-lookup"><span data-stu-id="47193-163">Web API protocols (http, https).</span></span>
<span data-ttu-id="47193-164">Protokolle, über die API verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="47193-164">Protocols over which API is made available.</span></span>
<span data-ttu-id="47193-165">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="47193-165">This parameter is required.</span></span>
<span data-ttu-id="47193-166">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="47193-166">Default value is $null.</span></span>

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

### <span data-ttu-id="47193-167">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="47193-167">-ServiceUrl</span></span>
<span data-ttu-id="47193-168">Eine URL des Webdiensts, der die API verfügbar machen soll.</span><span class="sxs-lookup"><span data-stu-id="47193-168">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="47193-169">Diese URL wird nur von Azure API Management verwendet und nicht öffentlich gemacht.</span><span class="sxs-lookup"><span data-stu-id="47193-169">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="47193-170">Muss 1 bis 2.000 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="47193-170">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="47193-171">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="47193-171">This parameter is required.</span></span>

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

### <span data-ttu-id="47193-172">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="47193-172">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="47193-173">Name der Kopfzeile des Abonnementschlüssels.</span><span class="sxs-lookup"><span data-stu-id="47193-173">Subscription key header name.</span></span>
<span data-ttu-id="47193-174">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="47193-174">This parameter is optional.</span></span>
<span data-ttu-id="47193-175">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="47193-175">Default value is $null.</span></span>

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

### <span data-ttu-id="47193-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="47193-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="47193-177">Parametername der Abonnementschlüsselabfragezeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="47193-177">Subscription key query string parameter name.</span></span>
<span data-ttu-id="47193-178">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="47193-178">This parameter is optional.</span></span>
<span data-ttu-id="47193-179">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="47193-179">Default value is $null.</span></span>

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

### <span data-ttu-id="47193-180">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="47193-180">-SubscriptionRequired</span></span>
<span data-ttu-id="47193-181">Flag zum Erzwingen von "SubscriptionRequired" für Anforderungen an die API.</span><span class="sxs-lookup"><span data-stu-id="47193-181">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="47193-182">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="47193-182">This parameter is optional.</span></span>

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

### <span data-ttu-id="47193-183">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47193-183">-Confirm</span></span>
<span data-ttu-id="47193-184">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="47193-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47193-185">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="47193-185">-WhatIf</span></span>
<span data-ttu-id="47193-186">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47193-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47193-187">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47193-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47193-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47193-188">CommonParameters</span></span>
<span data-ttu-id="47193-189">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47193-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47193-190">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47193-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47193-191">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="47193-191">INPUTS</span></span>

### <span data-ttu-id="47193-192">System.String</span><span class="sxs-lookup"><span data-stu-id="47193-192">System.String</span></span>

### <span data-ttu-id="47193-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="47193-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="47193-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="47193-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="47193-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span><span class="sxs-lookup"><span data-stu-id="47193-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="47193-196">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="47193-196">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="47193-197">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="47193-197">OUTPUTS</span></span>

### <span data-ttu-id="47193-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="47193-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="47193-199">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="47193-199">NOTES</span></span>

## <span data-ttu-id="47193-200">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="47193-200">RELATED LINKS</span></span>

[<span data-ttu-id="47193-201">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="47193-201">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="47193-202">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="47193-202">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="47193-203">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="47193-203">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)