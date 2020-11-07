---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: fe9957c439a0ca54d290181b2b3ab8d85b74f696
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658156"
---
# <span data-ttu-id="4b124-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="4b124-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="4b124-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4b124-102">SYNOPSIS</span></span>
<span data-ttu-id="4b124-103">Ändert eine API-Revision</span><span class="sxs-lookup"><span data-stu-id="4b124-103">Modifies an API Revision</span></span>

## <span data-ttu-id="4b124-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b124-104">SYNTAX</span></span>

### <span data-ttu-id="4b124-105">Expanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="4b124-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 [-Name <String>] [-Description <String>] [-ServiceUrl <String>] [-Path <String>]
 [-Protocols <PsApiManagementSchema[]>] [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-OpenIdProviderId <String>] [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b124-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4b124-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b124-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b124-107">DESCRIPTION</span></span>
<span data-ttu-id="4b124-108">Das Cmdlet " **Satz-AzApiManagementApiRevision** " ändert eine Azure API Management-API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="4b124-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="4b124-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4b124-109">EXAMPLES</span></span>

### <span data-ttu-id="4b124-110">Beispiel 1 Ändern einer API-Revision</span><span class="sxs-lookup"><span data-stu-id="4b124-110">Example 1 Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="4b124-111">Das Cmdlet aktualisiert die `2` Revision der API `echo-api` mit einer neuen Beschreibung, einem neuen Protokoll und einem Pfad.</span><span class="sxs-lookup"><span data-stu-id="4b124-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="4b124-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b124-112">PARAMETERS</span></span>

### <span data-ttu-id="4b124-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4b124-113">-ApiId</span></span>
<span data-ttu-id="4b124-114">Bezeichner der vorhandenen API.</span><span class="sxs-lookup"><span data-stu-id="4b124-114">Identifier of existing API.</span></span>
<span data-ttu-id="4b124-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4b124-115">This parameter is required.</span></span>

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

### <span data-ttu-id="4b124-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="4b124-116">-ApiRevision</span></span>
<span data-ttu-id="4b124-117">Bezeichner der vorhandenen API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="4b124-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="4b124-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4b124-118">This parameter is required.</span></span>

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

### <span data-ttu-id="4b124-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="4b124-119">-AuthorizationScope</span></span>
<span data-ttu-id="4b124-120">OAuth-Vorgangsbereich</span><span class="sxs-lookup"><span data-stu-id="4b124-120">OAuth operations scope.</span></span>
<span data-ttu-id="4b124-121">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="4b124-121">This parameter is optional.</span></span>
<span data-ttu-id="4b124-122">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="4b124-122">Default value is $null.</span></span>

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

### <span data-ttu-id="4b124-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="4b124-123">-AuthorizationServerId</span></span>
<span data-ttu-id="4b124-124">OAuth-autorisierungsserver-ID.</span><span class="sxs-lookup"><span data-stu-id="4b124-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="4b124-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="4b124-125">This parameter is optional.</span></span>
<span data-ttu-id="4b124-126">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="4b124-126">Default value is $null.</span></span>
<span data-ttu-id="4b124-127">Muss angegeben werden, wenn AuthorizationScope angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4b124-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="4b124-128">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="4b124-128">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="4b124-129">OpenID Authorization Server-Mechanismus, mit dem das Zugriffstoken an die API übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="4b124-129">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="4b124-130">Weitere Informationen finden Sie unter http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="4b124-130">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="4b124-131">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="4b124-131">This parameter is optional.</span></span> <span data-ttu-id="4b124-132">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="4b124-132">Default value is $null.</span></span>

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

### <span data-ttu-id="4b124-133">-Context</span><span class="sxs-lookup"><span data-stu-id="4b124-133">-Context</span></span>
<span data-ttu-id="4b124-134">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="4b124-134">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4b124-135">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4b124-135">This parameter is required.</span></span>

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

### <span data-ttu-id="4b124-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b124-136">-DefaultProfile</span></span>
<span data-ttu-id="4b124-137">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4b124-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b124-138">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b124-138">-Description</span></span>
<span data-ttu-id="4b124-139">Web-API-Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="4b124-139">Web API description.</span></span>
<span data-ttu-id="4b124-140">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="4b124-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="4b124-141">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4b124-141">-InputObject</span></span>
<span data-ttu-id="4b124-142">Instanz von PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="4b124-142">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="4b124-143">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4b124-143">This parameter is required.</span></span>

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

### <span data-ttu-id="4b124-144">-Name</span><span class="sxs-lookup"><span data-stu-id="4b124-144">-Name</span></span>
<span data-ttu-id="4b124-145">Web-API-Name.</span><span class="sxs-lookup"><span data-stu-id="4b124-145">Web API name.</span></span>
<span data-ttu-id="4b124-146">Öffentlicher Name der API, wie er auf dem Entwickler-und Administratorportal angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4b124-146">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="4b124-147">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4b124-147">This parameter is required.</span></span>

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

### <span data-ttu-id="4b124-148">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="4b124-148">-OpenIdProviderId</span></span>
<span data-ttu-id="4b124-149">OpenID-autorisierungsserver-ID.</span><span class="sxs-lookup"><span data-stu-id="4b124-149">OpenId authorization server identifier.</span></span> <span data-ttu-id="4b124-150">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="4b124-150">This parameter is optional.</span></span> <span data-ttu-id="4b124-151">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="4b124-151">Default value is $null.</span></span> <span data-ttu-id="4b124-152">Muss angegeben werden, wenn BearerTokenSendingMethods angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4b124-152">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="4b124-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b124-153">-PassThru</span></span>
<span data-ttu-id="4b124-154">Wenn angegeben, wird eine Instanz des Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi-Typs, die die festgelegte API darstellt.</span><span class="sxs-lookup"><span data-stu-id="4b124-154">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="4b124-155">-Path</span><span class="sxs-lookup"><span data-stu-id="4b124-155">-Path</span></span>
<span data-ttu-id="4b124-156">Web-API-Pfad.</span><span class="sxs-lookup"><span data-stu-id="4b124-156">Web API Path.</span></span>
<span data-ttu-id="4b124-157">Der letzte Teil der öffentlichen URL der API.</span><span class="sxs-lookup"><span data-stu-id="4b124-157">Last part of the API's public URL.</span></span>
<span data-ttu-id="4b124-158">Diese URL wird von API-Consumern zum Senden von Anforderungen an den Webdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b124-158">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="4b124-159">Muss 1 bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="4b124-159">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="4b124-160">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="4b124-160">This parameter is optional.</span></span>
<span data-ttu-id="4b124-161">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="4b124-161">Default value is $null.</span></span>

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

### <span data-ttu-id="4b124-162">-Protokolle</span><span class="sxs-lookup"><span data-stu-id="4b124-162">-Protocols</span></span>
<span data-ttu-id="4b124-163">Web-API-Protokolle (http, HTTPS).</span><span class="sxs-lookup"><span data-stu-id="4b124-163">Web API protocols (http, https).</span></span>
<span data-ttu-id="4b124-164">Protokolle, über die API zur Verfügung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4b124-164">Protocols over which API is made available.</span></span>
<span data-ttu-id="4b124-165">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4b124-165">This parameter is required.</span></span>
<span data-ttu-id="4b124-166">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="4b124-166">Default value is $null.</span></span>

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

### <span data-ttu-id="4b124-167">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="4b124-167">-ServiceUrl</span></span>
<span data-ttu-id="4b124-168">Eine URL des Webdiensts, der die API verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="4b124-168">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="4b124-169">Diese URL wird nur von der Azure-API-Verwaltung verwendet und wird nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="4b124-169">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="4b124-170">Muss 1 bis 2000 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="4b124-170">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="4b124-171">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4b124-171">This parameter is required.</span></span>

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

### <span data-ttu-id="4b124-172">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="4b124-172">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="4b124-173">Name des Abonnementschlüssel Headers.</span><span class="sxs-lookup"><span data-stu-id="4b124-173">Subscription key header name.</span></span>
<span data-ttu-id="4b124-174">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="4b124-174">This parameter is optional.</span></span>
<span data-ttu-id="4b124-175">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="4b124-175">Default value is $null.</span></span>

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

### <span data-ttu-id="4b124-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="4b124-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="4b124-177">Parameter Name der Abfragezeichenfolge für den Abonnementschlüssel</span><span class="sxs-lookup"><span data-stu-id="4b124-177">Subscription key query string parameter name.</span></span>
<span data-ttu-id="4b124-178">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="4b124-178">This parameter is optional.</span></span>
<span data-ttu-id="4b124-179">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="4b124-179">Default value is $null.</span></span>

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

### <span data-ttu-id="4b124-180">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="4b124-180">-SubscriptionRequired</span></span>
<span data-ttu-id="4b124-181">Flag zum Erzwingen von SubscriptionRequired für Anforderungen an die API.</span><span class="sxs-lookup"><span data-stu-id="4b124-181">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="4b124-182">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="4b124-182">This parameter is optional.</span></span>

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

### <span data-ttu-id="4b124-183">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4b124-183">-Confirm</span></span>
<span data-ttu-id="4b124-184">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4b124-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b124-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b124-185">-WhatIf</span></span>
<span data-ttu-id="4b124-186">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4b124-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b124-187">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b124-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b124-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b124-188">CommonParameters</span></span>
<span data-ttu-id="4b124-189">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b124-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b124-190">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b124-190">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b124-191">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4b124-191">INPUTS</span></span>

### <span data-ttu-id="4b124-192">System. String</span><span class="sxs-lookup"><span data-stu-id="4b124-192">System.String</span></span>

### <span data-ttu-id="4b124-193">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4b124-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4b124-194">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4b124-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="4b124-195">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="4b124-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="4b124-196">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="4b124-196">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4b124-197">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4b124-197">OUTPUTS</span></span>

### <span data-ttu-id="4b124-198">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4b124-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="4b124-199">Notizen</span><span class="sxs-lookup"><span data-stu-id="4b124-199">NOTES</span></span>

## <span data-ttu-id="4b124-200">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4b124-200">RELATED LINKS</span></span>

[<span data-ttu-id="4b124-201">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="4b124-201">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="4b124-202">Neu – AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="4b124-202">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="4b124-203">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="4b124-203">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)