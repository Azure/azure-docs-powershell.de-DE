---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 482a558e469e3f8094e4b619ef61ec37f076f739
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004071"
---
# <span data-ttu-id="cb4c4-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cb4c4-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="cb4c4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cb4c4-102">SYNOPSIS</span></span>
<span data-ttu-id="cb4c4-103">Ändert eine API.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-103">Modifies an API.</span></span>

## <span data-ttu-id="cb4c4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb4c4-104">SYNTAX</span></span>

### <span data-ttu-id="cb4c4-105">Expanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="cb4c4-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb4c4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cb4c4-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb4c4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb4c4-107">DESCRIPTION</span></span>
<span data-ttu-id="cb4c4-108">Das Cmdlet " **Satz-AzApiManagementApi** " ändert eine Azure API-Verwaltungs-API.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="cb4c4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cb4c4-109">EXAMPLES</span></span>

### <span data-ttu-id="cb4c4-110">Beispiel 1 Ändern einer API</span><span class="sxs-lookup"><span data-stu-id="cb4c4-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="cb4c4-111">Beispiel 2 Hinzufügen einer API zu einem vorhandenen ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="cb4c4-111">Example 2 Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```

<span data-ttu-id="cb4c4-112">In diesem Beispiel wird eine API zu einem vorhandenen API-Versions Satz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-112">This example adds an API to an existing API Version Set</span></span>

### <span data-ttu-id="cb4c4-113">Beispiel 3 Ändern des Back-End-serviceUrl, auf das die API zeigt</span><span class="sxs-lookup"><span data-stu-id="cb4c4-113">Example 3 Change the Backend ServiceUrl where the API is pointing to</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$updatedApiServiceUrl = "http://newechoapi.cloudapp.net/updateapi"
PS C:\>$updatedApi = Set-AzApiManagementApi -Context $ApiMgmtContext -ApiId $echoApiId -ServiceUrl $updatedApiServiceUrl
```

<span data-ttu-id="cb4c4-114">In diesem Beispiel wird das serviceUrl aktualisiert `echo-api` , auf das verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-114">This example updates the ServiceUrl the `echo-api` is pointing to.</span></span>

## <span data-ttu-id="cb4c4-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb4c4-115">PARAMETERS</span></span>

### <span data-ttu-id="cb4c4-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="cb4c4-116">-ApiId</span></span>
<span data-ttu-id="cb4c4-117">Gibt die ID der zu ändernden API an.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-117">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="cb4c4-118">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="cb4c4-118">-AuthorizationScope</span></span>
<span data-ttu-id="cb4c4-119">Gibt den OAuth-Vorgangsbereich an.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-119">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="cb4c4-120">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-120">The default value is $Null.</span></span>

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

### <span data-ttu-id="cb4c4-121">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="cb4c4-121">-AuthorizationServerId</span></span>
<span data-ttu-id="cb4c4-122">Gibt den OAuth-autorisierungsserver-Bezeichner an.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-122">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="cb4c4-123">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-123">The default value is $Null.</span></span>
<span data-ttu-id="cb4c4-124">Sie müssen diesen Parameter angeben, wenn *AuthorizationScope* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-124">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="cb4c4-125">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="cb4c4-125">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="cb4c4-126">OpenID Authorization Server-Mechanismus, mit dem das Zugriffstoken an die API übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-126">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="cb4c4-127">Weitere Informationen finden Sie unter http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="cb4c4-127">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="cb4c4-128">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-128">This parameter is optional.</span></span> <span data-ttu-id="cb4c4-129">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-129">Default value is $null.</span></span>

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

### <span data-ttu-id="cb4c4-130">-Context</span><span class="sxs-lookup"><span data-stu-id="cb4c4-130">-Context</span></span>
<span data-ttu-id="cb4c4-131">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-131">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="cb4c4-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb4c4-132">-DefaultProfile</span></span>
<span data-ttu-id="cb4c4-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb4c4-134">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb4c4-134">-Description</span></span>
<span data-ttu-id="cb4c4-135">Gibt eine Beschreibung für die Web-API an.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-135">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="cb4c4-136">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cb4c4-136">-InputObject</span></span>
<span data-ttu-id="cb4c4-137">Instanz von PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="cb4c4-138">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-138">This parameter is required.</span></span>

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

### <span data-ttu-id="cb4c4-139">-Name</span><span class="sxs-lookup"><span data-stu-id="cb4c4-139">-Name</span></span>
<span data-ttu-id="cb4c4-140">Gibt den Namen der Web-API an.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-140">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="cb4c4-141">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="cb4c4-141">-OpenIdProviderId</span></span>
<span data-ttu-id="cb4c4-142">OpenID-autorisierungsserver-ID.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-142">OpenId authorization server identifier.</span></span> <span data-ttu-id="cb4c4-143">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-143">This parameter is optional.</span></span> <span data-ttu-id="cb4c4-144">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-144">Default value is $null.</span></span> <span data-ttu-id="cb4c4-145">Muss angegeben werden, wenn BearerTokenSendingMethods angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-145">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="cb4c4-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb4c4-146">-PassThru</span></span>
<span data-ttu-id="cb4c4-147">passthru</span><span class="sxs-lookup"><span data-stu-id="cb4c4-147">passthru</span></span>

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

### <span data-ttu-id="cb4c4-148">-Path</span><span class="sxs-lookup"><span data-stu-id="cb4c4-148">-Path</span></span>
<span data-ttu-id="cb4c4-149">Gibt den WebAPI-Pfad an, bei dem es sich um den letzten Teil der öffentlichen URL der API handelt.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-149">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="cb4c4-150">Diese URL wird von API-Consumern verwendet, um Anforderungen an den Webdienst zu senden, und muss ein bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-150">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="cb4c4-151">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-151">The default value is $Null.</span></span>

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

### <span data-ttu-id="cb4c4-152">-Protokolle</span><span class="sxs-lookup"><span data-stu-id="cb4c4-152">-Protocols</span></span>
<span data-ttu-id="cb4c4-153">Gibt ein Array von Web-API-Protokollen an.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-153">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="cb4c4-154">psdx_paramvalues http und HTTPS.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-154">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="cb4c4-155">Hierbei handelt es sich um die Webprotokolle, über die die API zur Verfügung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-155">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="cb4c4-156">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-156">The default value is $Null.</span></span>

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

### <span data-ttu-id="cb4c4-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="cb4c4-157">-ServiceUrl</span></span>
<span data-ttu-id="cb4c4-158">Gibt die URL des Webdiensts an, der die API verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-158">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="cb4c4-159">Diese URL wird nur von der Azure-API-Verwaltung verwendet und nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-159">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="cb4c4-160">Die URL muss ein bis 2000 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-160">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="cb4c4-161">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="cb4c4-161">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="cb4c4-162">Gibt den Namen des Abonnementschlüssel Headers an.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-162">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="cb4c4-163">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-163">The default value is $Null.</span></span>

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

### <span data-ttu-id="cb4c4-164">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="cb4c4-164">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="cb4c4-165">Gibt den Namen des Abfragezeichen folgen Parameters für den Abonnementschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-165">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="cb4c4-166">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-166">The default value is $Null.</span></span>

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

### <span data-ttu-id="cb4c4-167">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="cb4c4-167">-SubscriptionRequired</span></span>
<span data-ttu-id="cb4c4-168">Flag zum Erzwingen von SubscriptionRequired für Anforderungen an die API.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-168">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="cb4c4-169">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="cb4c4-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb4c4-170">CommonParameters</span></span>
<span data-ttu-id="cb4c4-171">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb4c4-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb4c4-172">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb4c4-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb4c4-173">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cb4c4-173">INPUTS</span></span>

### <span data-ttu-id="cb4c4-174">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cb4c4-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cb4c4-175">System. String</span><span class="sxs-lookup"><span data-stu-id="cb4c4-175">System.String</span></span>

### <span data-ttu-id="cb4c4-176">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cb4c4-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="cb4c4-177">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="cb4c4-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="cb4c4-178">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="cb4c4-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cb4c4-179">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cb4c4-179">OUTPUTS</span></span>

### <span data-ttu-id="cb4c4-180">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cb4c4-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="cb4c4-181">Notizen</span><span class="sxs-lookup"><span data-stu-id="cb4c4-181">NOTES</span></span>

## <span data-ttu-id="cb4c4-182">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cb4c4-182">RELATED LINKS</span></span>

[<span data-ttu-id="cb4c4-183">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cb4c4-183">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="cb4c4-184">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cb4c4-184">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="cb4c4-185">Importieren-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cb4c4-185">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="cb4c4-186">Neu – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cb4c4-186">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="cb4c4-187">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cb4c4-187">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


