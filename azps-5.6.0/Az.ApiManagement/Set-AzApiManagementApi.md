---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: cdef3f217cec1401457f2f25daa91edafd4850b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949011"
---
# <span data-ttu-id="17c28-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="17c28-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="17c28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17c28-102">SYNOPSIS</span></span>
<span data-ttu-id="17c28-103">Ändert eine API.</span><span class="sxs-lookup"><span data-stu-id="17c28-103">Modifies an API.</span></span>

## <span data-ttu-id="17c28-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17c28-104">SYNTAX</span></span>

### <span data-ttu-id="17c28-105">ExpandedParameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="17c28-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17c28-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="17c28-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17c28-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17c28-107">DESCRIPTION</span></span>
<span data-ttu-id="17c28-108">Das **Cmdlet Set-AzApiManagementApi** ändert eine Azure API-Verwaltungs-API.</span><span class="sxs-lookup"><span data-stu-id="17c28-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="17c28-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="17c28-109">EXAMPLES</span></span>

### <span data-ttu-id="17c28-110">Beispiel 1: Ändern einer API</span><span class="sxs-lookup"><span data-stu-id="17c28-110">Example 1: Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="17c28-111">Beispiel 2: Hinzufügen einer API zu einem vorhandenen ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="17c28-111">Example 2: Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```

<span data-ttu-id="17c28-112">In diesem Beispiel wird einem vorhandenen API-Versionssatz eine API hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="17c28-112">This example adds an API to an existing API Version Set</span></span>

### <span data-ttu-id="17c28-113">Beispiel 3: Ändern des Back-End-Diensts, auf den die API zeigt</span><span class="sxs-lookup"><span data-stu-id="17c28-113">Example 3: Change the Backend ServiceUrl where the API is pointing to</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$updatedApiServiceUrl = "http://newechoapi.cloudapp.net/updateapi"
PS C:\>$updatedApi = Set-AzApiManagementApi -Context $ApiMgmtContext -ApiId $echoApiId -ServiceUrl $updatedApiServiceUrl
```

<span data-ttu-id="17c28-114">In diesem Beispiel wird der ServiceUrl `echo-api` aktualisiert, auf den der zeigt.</span><span class="sxs-lookup"><span data-stu-id="17c28-114">This example updates the ServiceUrl the `echo-api` is pointing to.</span></span>

## <span data-ttu-id="17c28-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="17c28-115">PARAMETERS</span></span>

### <span data-ttu-id="17c28-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="17c28-116">-ApiId</span></span>
<span data-ttu-id="17c28-117">Gibt die ID der zu ändernden API an.</span><span class="sxs-lookup"><span data-stu-id="17c28-117">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="17c28-118">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="17c28-118">-AuthorizationScope</span></span>
<span data-ttu-id="17c28-119">Gibt den OAuth-Operationsbereich an.</span><span class="sxs-lookup"><span data-stu-id="17c28-119">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="17c28-120">Der Standardwert ist $Null.</span><span class="sxs-lookup"><span data-stu-id="17c28-120">The default value is $Null.</span></span>

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

### <span data-ttu-id="17c28-121">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="17c28-121">-AuthorizationServerId</span></span>
<span data-ttu-id="17c28-122">Gibt den OAuth-Autorisierungsserverbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="17c28-122">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="17c28-123">Der Standardwert ist $Null.</span><span class="sxs-lookup"><span data-stu-id="17c28-123">The default value is $Null.</span></span>
<span data-ttu-id="17c28-124">Sie müssen diesen Parameter angeben, wenn *AuthorizationScope* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="17c28-124">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="17c28-125">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="17c28-125">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="17c28-126">OpenId-Autorisierungsservermechanismus, über den das Zugriffstoken an die API übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="17c28-126">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="17c28-127">Weitere Informationen finden Sie unter http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="17c28-127">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="17c28-128">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="17c28-128">This parameter is optional.</span></span> <span data-ttu-id="17c28-129">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="17c28-129">Default value is $null.</span></span>

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

### <span data-ttu-id="17c28-130">-Context</span><span class="sxs-lookup"><span data-stu-id="17c28-130">-Context</span></span>
<span data-ttu-id="17c28-131">Gibt ein **PsApiManagementContext-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="17c28-131">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="17c28-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17c28-132">-DefaultProfile</span></span>
<span data-ttu-id="17c28-133">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17c28-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17c28-134">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17c28-134">-Description</span></span>
<span data-ttu-id="17c28-135">Gibt eine Beschreibung für die Web-API an.</span><span class="sxs-lookup"><span data-stu-id="17c28-135">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="17c28-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17c28-136">-InputObject</span></span>
<span data-ttu-id="17c28-137">Instanz von PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="17c28-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="17c28-138">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="17c28-138">This parameter is required.</span></span>

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

### <span data-ttu-id="17c28-139">-Name</span><span class="sxs-lookup"><span data-stu-id="17c28-139">-Name</span></span>
<span data-ttu-id="17c28-140">Gibt den Namen der Web-API an.</span><span class="sxs-lookup"><span data-stu-id="17c28-140">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="17c28-141">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="17c28-141">-OpenIdProviderId</span></span>
<span data-ttu-id="17c28-142">OpenId Authorization Server Identifier.</span><span class="sxs-lookup"><span data-stu-id="17c28-142">OpenId authorization server identifier.</span></span> <span data-ttu-id="17c28-143">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="17c28-143">This parameter is optional.</span></span> <span data-ttu-id="17c28-144">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="17c28-144">Default value is $null.</span></span> <span data-ttu-id="17c28-145">Muss angegeben werden, wenn BearerTokenSendingMethods angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="17c28-145">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="17c28-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17c28-146">-PassThru</span></span>
<span data-ttu-id="17c28-147">passthru</span><span class="sxs-lookup"><span data-stu-id="17c28-147">passthru</span></span>

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

### <span data-ttu-id="17c28-148">-Path</span><span class="sxs-lookup"><span data-stu-id="17c28-148">-Path</span></span>
<span data-ttu-id="17c28-149">Gibt den Web-API-Pfad an, der der letzte Teil der öffentlichen URL der API ist.</span><span class="sxs-lookup"><span data-stu-id="17c28-149">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="17c28-150">Diese URL wird von API-Konsumenten zum Senden von Anforderungen an den Webdienst verwendet und muss 1 bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="17c28-150">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="17c28-151">Der Standardwert ist $Null.</span><span class="sxs-lookup"><span data-stu-id="17c28-151">The default value is $Null.</span></span>

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

### <span data-ttu-id="17c28-152">-Protokolle</span><span class="sxs-lookup"><span data-stu-id="17c28-152">-Protocols</span></span>
<span data-ttu-id="17c28-153">Gibt ein Array von Web-API-Protokollen an.</span><span class="sxs-lookup"><span data-stu-id="17c28-153">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="17c28-154">psdx_paramvalues http und https.</span><span class="sxs-lookup"><span data-stu-id="17c28-154">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="17c28-155">Dies sind die Webprotokolle, über die die API verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="17c28-155">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="17c28-156">Der Standardwert ist $Null.</span><span class="sxs-lookup"><span data-stu-id="17c28-156">The default value is $Null.</span></span>

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

### <span data-ttu-id="17c28-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="17c28-157">-ServiceUrl</span></span>
<span data-ttu-id="17c28-158">Gibt die URL des Webdiensts an, der die API verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="17c28-158">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="17c28-159">Diese URL wird nur von Azure API Management verwendet und nicht öffentlich gemacht.</span><span class="sxs-lookup"><span data-stu-id="17c28-159">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="17c28-160">Die URL muss 1 bis 2.000 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="17c28-160">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="17c28-161">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="17c28-161">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="17c28-162">Gibt den Namen des Abonnementschlüsselkopfs an.</span><span class="sxs-lookup"><span data-stu-id="17c28-162">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="17c28-163">Der Standardwert ist $Null.</span><span class="sxs-lookup"><span data-stu-id="17c28-163">The default value is $Null.</span></span>

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

### <span data-ttu-id="17c28-164">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="17c28-164">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="17c28-165">Gibt den Namen des Zeichenfolgenparameters für die Abfrageabfrage des Abonnementschlüssels an.</span><span class="sxs-lookup"><span data-stu-id="17c28-165">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="17c28-166">Der Standardwert ist $Null.</span><span class="sxs-lookup"><span data-stu-id="17c28-166">The default value is $Null.</span></span>

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

### <span data-ttu-id="17c28-167">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="17c28-167">-SubscriptionRequired</span></span>
<span data-ttu-id="17c28-168">Kennzeichnen, um SubscriptionRequired für Anforderungen an die Api zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="17c28-168">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="17c28-169">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="17c28-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="17c28-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17c28-170">CommonParameters</span></span>
<span data-ttu-id="17c28-171">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17c28-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17c28-172">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17c28-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17c28-173">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="17c28-173">INPUTS</span></span>

### <span data-ttu-id="17c28-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="17c28-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="17c28-175">System.String</span><span class="sxs-lookup"><span data-stu-id="17c28-175">System.String</span></span>

### <span data-ttu-id="17c28-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="17c28-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="17c28-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span><span class="sxs-lookup"><span data-stu-id="17c28-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="17c28-178">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="17c28-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="17c28-179">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="17c28-179">OUTPUTS</span></span>

### <span data-ttu-id="17c28-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="17c28-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="17c28-181">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="17c28-181">NOTES</span></span>

## <span data-ttu-id="17c28-182">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="17c28-182">RELATED LINKS</span></span>

[<span data-ttu-id="17c28-183">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="17c28-183">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="17c28-184">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="17c28-184">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="17c28-185">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="17c28-185">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="17c28-186">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="17c28-186">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="17c28-187">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="17c28-187">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


