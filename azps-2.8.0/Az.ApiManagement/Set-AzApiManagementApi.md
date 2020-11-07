---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 973dc9bac629ee9a82b7624053f689bf7884fd8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658159"
---
# <span data-ttu-id="8ec2b-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8ec2b-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="8ec2b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8ec2b-102">SYNOPSIS</span></span>
<span data-ttu-id="8ec2b-103">Ändert eine API.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-103">Modifies an API.</span></span>

## <span data-ttu-id="8ec2b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ec2b-104">SYNTAX</span></span>

### <span data-ttu-id="8ec2b-105">Expanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="8ec2b-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ec2b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8ec2b-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ec2b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ec2b-107">DESCRIPTION</span></span>
<span data-ttu-id="8ec2b-108">Das Cmdlet " **Satz-AzApiManagementApi** " ändert eine Azure API-Verwaltungs-API.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="8ec2b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ec2b-109">EXAMPLES</span></span>

### <span data-ttu-id="8ec2b-110">Beispiel 1 Ändern einer API</span><span class="sxs-lookup"><span data-stu-id="8ec2b-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="8ec2b-111">Beispiel 2 Hinzufügen einer API zu einem vorhandenen ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="8ec2b-111">Example 2 Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```
<span data-ttu-id="8ec2b-112">In diesem Beispiel wird eine API zu einem vorhandenen API-Versions Satz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-112">This example adds an API to an existing API Version Set</span></span>

## <span data-ttu-id="8ec2b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ec2b-113">PARAMETERS</span></span>

### <span data-ttu-id="8ec2b-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8ec2b-114">-ApiId</span></span>
<span data-ttu-id="8ec2b-115">Gibt die ID der zu ändernden API an.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-115">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="8ec2b-116">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="8ec2b-116">-AuthorizationScope</span></span>
<span data-ttu-id="8ec2b-117">Gibt den OAuth-Vorgangsbereich an.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-117">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="8ec2b-118">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-118">The default value is $Null.</span></span>

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

### <span data-ttu-id="8ec2b-119">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="8ec2b-119">-AuthorizationServerId</span></span>
<span data-ttu-id="8ec2b-120">Gibt den OAuth-autorisierungsserver-Bezeichner an.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-120">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="8ec2b-121">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-121">The default value is $Null.</span></span>
<span data-ttu-id="8ec2b-122">Sie müssen diesen Parameter angeben, wenn *AuthorizationScope* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-122">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="8ec2b-123">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="8ec2b-123">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="8ec2b-124">OpenID Authorization Server-Mechanismus, mit dem das Zugriffstoken an die API übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-124">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="8ec2b-125">Weitere Informationen finden Sie unter http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="8ec2b-125">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="8ec2b-126">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-126">This parameter is optional.</span></span> <span data-ttu-id="8ec2b-127">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-127">Default value is $null.</span></span>

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

### <span data-ttu-id="8ec2b-128">-Context</span><span class="sxs-lookup"><span data-stu-id="8ec2b-128">-Context</span></span>
<span data-ttu-id="8ec2b-129">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-129">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8ec2b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ec2b-130">-DefaultProfile</span></span>
<span data-ttu-id="8ec2b-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ec2b-132">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ec2b-132">-Description</span></span>
<span data-ttu-id="8ec2b-133">Gibt eine Beschreibung für die Web-API an.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-133">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="8ec2b-134">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8ec2b-134">-InputObject</span></span>
<span data-ttu-id="8ec2b-135">Instanz von PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-135">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="8ec2b-136">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-136">This parameter is required.</span></span>

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

### <span data-ttu-id="8ec2b-137">-Name</span><span class="sxs-lookup"><span data-stu-id="8ec2b-137">-Name</span></span>
<span data-ttu-id="8ec2b-138">Gibt den Namen der Web-API an.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-138">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="8ec2b-139">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="8ec2b-139">-OpenIdProviderId</span></span>
<span data-ttu-id="8ec2b-140">OpenID-autorisierungsserver-ID.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-140">OpenId authorization server identifier.</span></span> <span data-ttu-id="8ec2b-141">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-141">This parameter is optional.</span></span> <span data-ttu-id="8ec2b-142">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-142">Default value is $null.</span></span> <span data-ttu-id="8ec2b-143">Muss angegeben werden, wenn BearerTokenSendingMethods angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-143">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="8ec2b-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ec2b-144">-PassThru</span></span>
<span data-ttu-id="8ec2b-145">passthru</span><span class="sxs-lookup"><span data-stu-id="8ec2b-145">passthru</span></span>

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

### <span data-ttu-id="8ec2b-146">-Path</span><span class="sxs-lookup"><span data-stu-id="8ec2b-146">-Path</span></span>
<span data-ttu-id="8ec2b-147">Gibt den WebAPI-Pfad an, bei dem es sich um den letzten Teil der öffentlichen URL der API handelt.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-147">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="8ec2b-148">Diese URL wird von API-Consumern verwendet, um Anforderungen an den Webdienst zu senden, und muss ein bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-148">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="8ec2b-149">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="8ec2b-150">-Protokolle</span><span class="sxs-lookup"><span data-stu-id="8ec2b-150">-Protocols</span></span>
<span data-ttu-id="8ec2b-151">Gibt ein Array von Web-API-Protokollen an.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-151">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="8ec2b-152">psdx_paramvalues http und HTTPS.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-152">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="8ec2b-153">Hierbei handelt es sich um die Webprotokolle, über die die API zur Verfügung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-153">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="8ec2b-154">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-154">The default value is $Null.</span></span>

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

### <span data-ttu-id="8ec2b-155">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="8ec2b-155">-ServiceUrl</span></span>
<span data-ttu-id="8ec2b-156">Gibt die URL des Webdiensts an, der die API verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-156">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="8ec2b-157">Diese URL wird nur von der Azure-API-Verwaltung verwendet und nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-157">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="8ec2b-158">Die URL muss ein bis 2000 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-158">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="8ec2b-159">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="8ec2b-159">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="8ec2b-160">Gibt den Namen des Abonnementschlüssel Headers an.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-160">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="8ec2b-161">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-161">The default value is $Null.</span></span>

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

### <span data-ttu-id="8ec2b-162">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="8ec2b-162">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="8ec2b-163">Gibt den Namen des Abfragezeichen folgen Parameters für den Abonnementschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-163">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="8ec2b-164">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-164">The default value is $Null.</span></span>

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

### <span data-ttu-id="8ec2b-165">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="8ec2b-165">-SubscriptionRequired</span></span>
<span data-ttu-id="8ec2b-166">Flag zum Erzwingen von SubscriptionRequired für Anforderungen an die API.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-166">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="8ec2b-167">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-167">This parameter is optional.</span></span>

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

### <span data-ttu-id="8ec2b-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ec2b-168">CommonParameters</span></span>
<span data-ttu-id="8ec2b-169">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ec2b-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ec2b-170">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ec2b-170">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ec2b-171">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8ec2b-171">INPUTS</span></span>

### <span data-ttu-id="8ec2b-172">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8ec2b-172">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8ec2b-173">System. String</span><span class="sxs-lookup"><span data-stu-id="8ec2b-173">System.String</span></span>

### <span data-ttu-id="8ec2b-174">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8ec2b-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="8ec2b-175">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="8ec2b-175">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="8ec2b-176">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="8ec2b-176">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8ec2b-177">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8ec2b-177">OUTPUTS</span></span>

### <span data-ttu-id="8ec2b-178">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8ec2b-178">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="8ec2b-179">Notizen</span><span class="sxs-lookup"><span data-stu-id="8ec2b-179">NOTES</span></span>

## <span data-ttu-id="8ec2b-180">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8ec2b-180">RELATED LINKS</span></span>

[<span data-ttu-id="8ec2b-181">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8ec2b-181">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="8ec2b-182">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8ec2b-182">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="8ec2b-183">Importieren-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8ec2b-183">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="8ec2b-184">Neu – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8ec2b-184">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="8ec2b-185">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8ec2b-185">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


