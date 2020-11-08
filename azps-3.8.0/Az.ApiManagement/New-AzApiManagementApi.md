---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: c9c0ab0ed8b932892f2bea27ff811197b808b86b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005206"
---
# <span data-ttu-id="6659f-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6659f-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="6659f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6659f-102">SYNOPSIS</span></span>
<span data-ttu-id="6659f-103">Erstellt eine API.</span><span class="sxs-lookup"><span data-stu-id="6659f-103">Creates an API.</span></span>

## <span data-ttu-id="6659f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6659f-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-SubscriptionRequired]
 [-ApiVersionDescription <String>] [-ApiVersionSetId <String>] [-ApiVersion <String>] [-SourceApiId <String>]
 [-SourceApiRevision <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6659f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6659f-105">DESCRIPTION</span></span>
<span data-ttu-id="6659f-106">Das Cmdlet **New-AzApiManagementApi** erstellt eine Azure API-Verwaltungs-API.</span><span class="sxs-lookup"><span data-stu-id="6659f-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="6659f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6659f-107">EXAMPLES</span></span>

### <span data-ttu-id="6659f-108">Beispiel 1: Erstellen einer API</span><span class="sxs-lookup"><span data-stu-id="6659f-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="6659f-109">Dieser Befehl erstellt eine API mit dem Namen EchoApi mit der angegebenen URL.</span><span class="sxs-lookup"><span data-stu-id="6659f-109">This command creates an API named EchoApi with the specified URL.</span></span>

### <span data-ttu-id="6659f-110">Beispiel 1: Erstellen einer API durch Kopieren aller Vorgänge, Tags, Produkte und Richtlinien aus der Echo-API und in eine ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="6659f-110">Example 1: Create an API by copying all operation, Tags, Products and Policies from echo-api and into an ApiVersionSet</span></span>
```powershell
PS D:\github\azure-powershell>$context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso
PS D:\github\azure-powershell>$versionSet = Get-AzApiManagementApiVersionSet -Context $context -ApiVersionSetId "xmsVersionSet"
PS D:\github\azure-powershell> New-AzApiManagementApi -Context $context -Name "echoapiv4" -Description "Create Echo Api V4" -SubscriptionRequired -ServiceUrl "https://echoapi.cloudapp.net/v4" -Path "echov3" -Protocols @("http", "https") -ApiVersionSetId $versionSet.ApiVersionSetId -SourceApiId "echo-api" -ApiVersion "v4"


ApiId                         : 691b7d410125414a929c108541c60e06
Name                          : echoapiv4
Description                   : Create Echo Api V4
ServiceUrl                    : https://echoapi.cloudapp.net/v4 
Path                          : echov3
ApiType                       : http
Protocols                     : {Http, Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    : v4
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          : True
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apiVersionSets/xmsVersionSet
Id                            : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apis/691b7d410125414a929c108541c60e06    
ResourceGroupName             : Api-Default-West-US
ServiceName                   : contoso
```

<span data-ttu-id="6659f-111">Dieser Befehl erstellt eine API `echoapiv3` in ApiVersionSet `xmsVersionSet` und kopiert alle Vorgänge, Tags und Richtlinien aus der Quell-API `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="6659f-111">This command creates an API `echoapiv3` in ApiVersionSet `xmsVersionSet` and copies all operation, Tags and Policies from source Api `echo-api`.</span></span> <span data-ttu-id="6659f-112">Sie überschreibt die SubscriptionRequired, serviceUrl, Path, Protocols</span><span class="sxs-lookup"><span data-stu-id="6659f-112">It overrides the SubscriptionRequired, ServiceUrl, Path, Protocols</span></span>

## <span data-ttu-id="6659f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6659f-113">PARAMETERS</span></span>

### <span data-ttu-id="6659f-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6659f-114">-ApiId</span></span>
<span data-ttu-id="6659f-115">Gibt die ID der zu erstellende API an.</span><span class="sxs-lookup"><span data-stu-id="6659f-115">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="6659f-116">Wenn Sie diesen Parameter nicht angeben, generiert dieses Cmdlet eine ID für Sie.</span><span class="sxs-lookup"><span data-stu-id="6659f-116">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="6659f-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6659f-117">-ApiVersion</span></span>
<span data-ttu-id="6659f-118">API-Version der zu erstellende API.</span><span class="sxs-lookup"><span data-stu-id="6659f-118">Api Version of the Api to create.</span></span> <span data-ttu-id="6659f-119">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6659f-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="6659f-120">-ApiVersionDescription</span><span class="sxs-lookup"><span data-stu-id="6659f-120">-ApiVersionDescription</span></span>
<span data-ttu-id="6659f-121">Beschreibung der API-Version.</span><span class="sxs-lookup"><span data-stu-id="6659f-121">Api Version Description.</span></span> <span data-ttu-id="6659f-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6659f-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="6659f-123">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="6659f-123">-ApiVersionSetId</span></span>
<span data-ttu-id="6659f-124">Ein Ressourcenbezeichner für den verknüpften API-Versions Satz.</span><span class="sxs-lookup"><span data-stu-id="6659f-124">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="6659f-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6659f-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="6659f-126">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="6659f-126">-AuthorizationScope</span></span>
<span data-ttu-id="6659f-127">Gibt den OAuth-Vorgangsbereich an.</span><span class="sxs-lookup"><span data-stu-id="6659f-127">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="6659f-128">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="6659f-128">The default value is $Null.</span></span>

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

### <span data-ttu-id="6659f-129">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="6659f-129">-AuthorizationServerId</span></span>
<span data-ttu-id="6659f-130">Gibt die OAuth-autorisierungsserver-ID an.</span><span class="sxs-lookup"><span data-stu-id="6659f-130">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="6659f-131">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="6659f-131">The default value is $Null.</span></span>
<span data-ttu-id="6659f-132">Sie müssen diesen Parameter angeben, wenn *AuthorizationScope* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="6659f-132">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="6659f-133">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="6659f-133">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="6659f-134">OpenID Authorization Server-Mechanismus, mit dem das Zugriffstoken an die API übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="6659f-134">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="6659f-135">Weitere Informationen finden Sie unter http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="6659f-135">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="6659f-136">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6659f-136">This parameter is optional.</span></span> <span data-ttu-id="6659f-137">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="6659f-137">Default value is $null.</span></span>

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

### <span data-ttu-id="6659f-138">-Context</span><span class="sxs-lookup"><span data-stu-id="6659f-138">-Context</span></span>
<span data-ttu-id="6659f-139">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="6659f-139">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6659f-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6659f-140">-DefaultProfile</span></span>
<span data-ttu-id="6659f-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6659f-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6659f-142">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6659f-142">-Description</span></span>
<span data-ttu-id="6659f-143">Gibt eine Beschreibung für die Web-API an.</span><span class="sxs-lookup"><span data-stu-id="6659f-143">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="6659f-144">-Name</span><span class="sxs-lookup"><span data-stu-id="6659f-144">-Name</span></span>
<span data-ttu-id="6659f-145">Gibt den Namen der Web-API an.</span><span class="sxs-lookup"><span data-stu-id="6659f-145">Specifies the name of the web API.</span></span>
<span data-ttu-id="6659f-146">Hierbei handelt es sich um den öffentlichen Namen der API, wie er auf dem Entwickler-und Administratorportal angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6659f-146">This is the public name of the API as it appears on the developer and admin portals.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6659f-147">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="6659f-147">-OpenIdProviderId</span></span>
<span data-ttu-id="6659f-148">OpenID-autorisierungsserver-ID.</span><span class="sxs-lookup"><span data-stu-id="6659f-148">OpenId authorization server identifier.</span></span> <span data-ttu-id="6659f-149">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6659f-149">This parameter is optional.</span></span> <span data-ttu-id="6659f-150">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="6659f-150">Default value is $null.</span></span> <span data-ttu-id="6659f-151">Muss angegeben werden, wenn BearerTokenSendingMethods angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="6659f-151">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="6659f-152">-Path</span><span class="sxs-lookup"><span data-stu-id="6659f-152">-Path</span></span>
<span data-ttu-id="6659f-153">Gibt den WebAPI-Pfad an, bei dem es sich um den letzten Teil der öffentlichen URL der API handelt, der dem Feld "URL-Suffix" für WebAPI im Administratorportal entspricht.</span><span class="sxs-lookup"><span data-stu-id="6659f-153">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="6659f-154">Diese URL wird von API-Consumern verwendet, um Anforderungen an den Webdienst zu senden, und muss ein bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="6659f-154">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="6659f-155">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="6659f-155">The default value is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6659f-156">-ProductIDs</span><span class="sxs-lookup"><span data-stu-id="6659f-156">-ProductIds</span></span>
<span data-ttu-id="6659f-157">Gibt ein Array von Produkt-IDs an, dem die neue API hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6659f-157">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="6659f-158">-Protokolle</span><span class="sxs-lookup"><span data-stu-id="6659f-158">-Protocols</span></span>
<span data-ttu-id="6659f-159">Gibt ein Array von Web-API-Protokollen an.</span><span class="sxs-lookup"><span data-stu-id="6659f-159">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="6659f-160">Gültige Werte sind http, HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6659f-160">Valid values are http, https.</span></span>
<span data-ttu-id="6659f-161">Hierbei handelt es sich um die Webprotokolle, über die die API zur Verfügung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6659f-161">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="6659f-162">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="6659f-162">The default value is $Null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6659f-163">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="6659f-163">-ServiceUrl</span></span>
<span data-ttu-id="6659f-164">Gibt die URL des Webdiensts an, der die API verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="6659f-164">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="6659f-165">Diese URL wird nur von der Azure-API-Verwaltung verwendet und nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="6659f-165">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="6659f-166">Die URL muss ein bis 2000 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="6659f-166">The URL must be one to 2000 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6659f-167">-SourceApiId</span><span class="sxs-lookup"><span data-stu-id="6659f-167">-SourceApiId</span></span>
<span data-ttu-id="6659f-168">API-Bezeichner der Quell-API.</span><span class="sxs-lookup"><span data-stu-id="6659f-168">Api identifier of the source API.</span></span> <span data-ttu-id="6659f-169">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6659f-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="6659f-170">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="6659f-170">-SourceApiRevision</span></span>
<span data-ttu-id="6659f-171">API-Revision der Quell-API.</span><span class="sxs-lookup"><span data-stu-id="6659f-171">Api Revision of the source API.</span></span> <span data-ttu-id="6659f-172">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6659f-172">This parameter is optional.</span></span>

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

### <span data-ttu-id="6659f-173">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="6659f-173">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="6659f-174">Gibt den Namen des Abonnementschlüssel Headers an.</span><span class="sxs-lookup"><span data-stu-id="6659f-174">Specifies the subscription key header name.</span></span>
<span data-ttu-id="6659f-175">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="6659f-175">The default value is $Null.</span></span>

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

### <span data-ttu-id="6659f-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="6659f-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="6659f-177">Gibt den Abfragezeichenfolgenparameter Namen für den Abonnementschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="6659f-177">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="6659f-178">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="6659f-178">The default value is $Null.</span></span>

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

### <span data-ttu-id="6659f-179">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="6659f-179">-SubscriptionRequired</span></span>
<span data-ttu-id="6659f-180">Flag zum Erzwingen von SubscriptionRequired für Anforderungen an die API.</span><span class="sxs-lookup"><span data-stu-id="6659f-180">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="6659f-181">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6659f-181">This parameter is optional.</span></span>

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

### <span data-ttu-id="6659f-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6659f-182">CommonParameters</span></span>
<span data-ttu-id="6659f-183">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6659f-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6659f-184">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6659f-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6659f-185">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6659f-185">INPUTS</span></span>

### <span data-ttu-id="6659f-186">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6659f-186">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6659f-187">System. String</span><span class="sxs-lookup"><span data-stu-id="6659f-187">System.String</span></span>

### <span data-ttu-id="6659f-188">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="6659f-188">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="6659f-189">System. String []</span><span class="sxs-lookup"><span data-stu-id="6659f-189">System.String[]</span></span>

## <span data-ttu-id="6659f-190">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6659f-190">OUTPUTS</span></span>

### <span data-ttu-id="6659f-191">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6659f-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="6659f-192">Notizen</span><span class="sxs-lookup"><span data-stu-id="6659f-192">NOTES</span></span>

## <span data-ttu-id="6659f-193">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6659f-193">RELATED LINKS</span></span>

[<span data-ttu-id="6659f-194">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6659f-194">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="6659f-195">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6659f-195">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="6659f-196">Importieren-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6659f-196">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="6659f-197">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6659f-197">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="6659f-198">Satz-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6659f-198">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


