---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: 3312c725d63bcb42aab7d82144c5a8f6f8e67641
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009451"
---
# <span data-ttu-id="3674b-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3674b-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="3674b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3674b-102">SYNOPSIS</span></span>
<span data-ttu-id="3674b-103">Erstellt eine API.</span><span class="sxs-lookup"><span data-stu-id="3674b-103">Creates an API.</span></span>

## <span data-ttu-id="3674b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3674b-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-SubscriptionRequired]
 [-ApiVersionDescription <String>] [-ApiVersionSetId <String>] [-ApiVersion <String>] [-SourceApiId <String>]
 [-SourceApiRevision <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3674b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3674b-105">DESCRIPTION</span></span>
<span data-ttu-id="3674b-106">Das Cmdlet **New-AzApiManagementApi** erstellt eine Azure API-Verwaltungs-API.</span><span class="sxs-lookup"><span data-stu-id="3674b-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="3674b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3674b-107">EXAMPLES</span></span>

### <span data-ttu-id="3674b-108">Beispiel 1: Erstellen einer API</span><span class="sxs-lookup"><span data-stu-id="3674b-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="3674b-109">Dieser Befehl erstellt eine API mit dem Namen EchoApi mit der angegebenen URL.</span><span class="sxs-lookup"><span data-stu-id="3674b-109">This command creates an API named EchoApi with the specified URL.</span></span>

### <span data-ttu-id="3674b-110">Beispiel 2: Erstellen einer API durch Kopieren aller Vorgänge, Tags, Produkte und Richtlinien aus der Echo-API und in eine ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="3674b-110">Example 2: Create an API by copying all operation, Tags, Products and Policies from echo-api and into an ApiVersionSet</span></span>
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

<span data-ttu-id="3674b-111">Dieser Befehl erstellt eine API `echoapiv3` in ApiVersionSet `xmsVersionSet` und kopiert alle Vorgänge, Tags und Richtlinien aus der Quell-API `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="3674b-111">This command creates an API `echoapiv3` in ApiVersionSet `xmsVersionSet` and copies all operation, Tags and Policies from source Api `echo-api`.</span></span> <span data-ttu-id="3674b-112">Sie überschreibt die SubscriptionRequired, serviceUrl, Path, Protocols</span><span class="sxs-lookup"><span data-stu-id="3674b-112">It overrides the SubscriptionRequired, ServiceUrl, Path, Protocols</span></span>

### <span data-ttu-id="3674b-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="3674b-113">Example 3</span></span>

<span data-ttu-id="3674b-114">Erstellt eine API.</span><span class="sxs-lookup"><span data-stu-id="3674b-114">Creates an API.</span></span> <span data-ttu-id="3674b-115">automatisch</span><span class="sxs-lookup"><span data-stu-id="3674b-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzApiManagementApi -ApiId '0001' -Context <PsApiManagementContext> -Name 'Echo api' -Path 'echov3' -Protocols Http -ServiceUrl 'https://contoso.com/apis/echo'
```

## <span data-ttu-id="3674b-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="3674b-116">PARAMETERS</span></span>

### <span data-ttu-id="3674b-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3674b-117">-ApiId</span></span>
<span data-ttu-id="3674b-118">Gibt die ID der zu erstellende API an.</span><span class="sxs-lookup"><span data-stu-id="3674b-118">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="3674b-119">Wenn Sie diesen Parameter nicht angeben, generiert dieses Cmdlet eine ID für Sie.</span><span class="sxs-lookup"><span data-stu-id="3674b-119">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="3674b-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3674b-120">-ApiVersion</span></span>
<span data-ttu-id="3674b-121">API-Version der zu erstellende API.</span><span class="sxs-lookup"><span data-stu-id="3674b-121">Api Version of the Api to create.</span></span> <span data-ttu-id="3674b-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="3674b-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="3674b-123">-ApiVersionDescription</span><span class="sxs-lookup"><span data-stu-id="3674b-123">-ApiVersionDescription</span></span>
<span data-ttu-id="3674b-124">Beschreibung der API-Version.</span><span class="sxs-lookup"><span data-stu-id="3674b-124">Api Version Description.</span></span> <span data-ttu-id="3674b-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="3674b-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="3674b-126">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="3674b-126">-ApiVersionSetId</span></span>
<span data-ttu-id="3674b-127">Ein Ressourcenbezeichner für den verknüpften API-Versions Satz.</span><span class="sxs-lookup"><span data-stu-id="3674b-127">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="3674b-128">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="3674b-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="3674b-129">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="3674b-129">-AuthorizationScope</span></span>
<span data-ttu-id="3674b-130">Gibt den OAuth-Vorgangsbereich an.</span><span class="sxs-lookup"><span data-stu-id="3674b-130">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="3674b-131">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="3674b-131">The default value is $Null.</span></span>

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

### <span data-ttu-id="3674b-132">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="3674b-132">-AuthorizationServerId</span></span>
<span data-ttu-id="3674b-133">Gibt die OAuth-autorisierungsserver-ID an.</span><span class="sxs-lookup"><span data-stu-id="3674b-133">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="3674b-134">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="3674b-134">The default value is $Null.</span></span>
<span data-ttu-id="3674b-135">Sie müssen diesen Parameter angeben, wenn *AuthorizationScope* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="3674b-135">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="3674b-136">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="3674b-136">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="3674b-137">OpenID Authorization Server-Mechanismus, mit dem das Zugriffstoken an die API übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="3674b-137">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="3674b-138">Weitere Informationen finden Sie unter http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="3674b-138">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="3674b-139">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="3674b-139">This parameter is optional.</span></span> <span data-ttu-id="3674b-140">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="3674b-140">Default value is $null.</span></span>

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

### <span data-ttu-id="3674b-141">-Context</span><span class="sxs-lookup"><span data-stu-id="3674b-141">-Context</span></span>
<span data-ttu-id="3674b-142">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="3674b-142">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3674b-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3674b-143">-DefaultProfile</span></span>
<span data-ttu-id="3674b-144">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3674b-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3674b-145">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3674b-145">-Description</span></span>
<span data-ttu-id="3674b-146">Gibt eine Beschreibung für die Web-API an.</span><span class="sxs-lookup"><span data-stu-id="3674b-146">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="3674b-147">-Name</span><span class="sxs-lookup"><span data-stu-id="3674b-147">-Name</span></span>
<span data-ttu-id="3674b-148">Gibt den Namen der Web-API an.</span><span class="sxs-lookup"><span data-stu-id="3674b-148">Specifies the name of the web API.</span></span>
<span data-ttu-id="3674b-149">Hierbei handelt es sich um den öffentlichen Namen der API, wie er auf dem Entwickler-und Administratorportal angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3674b-149">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="3674b-150">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="3674b-150">-OpenIdProviderId</span></span>
<span data-ttu-id="3674b-151">OpenID-autorisierungsserver-ID.</span><span class="sxs-lookup"><span data-stu-id="3674b-151">OpenId authorization server identifier.</span></span> <span data-ttu-id="3674b-152">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="3674b-152">This parameter is optional.</span></span> <span data-ttu-id="3674b-153">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="3674b-153">Default value is $null.</span></span> <span data-ttu-id="3674b-154">Muss angegeben werden, wenn BearerTokenSendingMethods angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="3674b-154">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="3674b-155">-Path</span><span class="sxs-lookup"><span data-stu-id="3674b-155">-Path</span></span>
<span data-ttu-id="3674b-156">Gibt den WebAPI-Pfad an, bei dem es sich um den letzten Teil der öffentlichen URL der API handelt, der dem Feld "URL-Suffix" für WebAPI im Administratorportal entspricht.</span><span class="sxs-lookup"><span data-stu-id="3674b-156">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="3674b-157">Diese URL wird von API-Consumern verwendet, um Anforderungen an den Webdienst zu senden, und muss ein bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="3674b-157">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="3674b-158">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="3674b-158">The default value is $Null.</span></span>

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

### <span data-ttu-id="3674b-159">-ProductIDs</span><span class="sxs-lookup"><span data-stu-id="3674b-159">-ProductIds</span></span>
<span data-ttu-id="3674b-160">Gibt ein Array von Produkt-IDs an, dem die neue API hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3674b-160">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="3674b-161">-Protokolle</span><span class="sxs-lookup"><span data-stu-id="3674b-161">-Protocols</span></span>
<span data-ttu-id="3674b-162">Gibt ein Array von Web-API-Protokollen an.</span><span class="sxs-lookup"><span data-stu-id="3674b-162">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="3674b-163">Gültige Werte sind http, HTTPS.</span><span class="sxs-lookup"><span data-stu-id="3674b-163">Valid values are http, https.</span></span>
<span data-ttu-id="3674b-164">Hierbei handelt es sich um die Webprotokolle, über die die API zur Verfügung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3674b-164">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="3674b-165">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="3674b-165">The default value is $Null.</span></span>

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

### <span data-ttu-id="3674b-166">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="3674b-166">-ServiceUrl</span></span>
<span data-ttu-id="3674b-167">Gibt die URL des Webdiensts an, der die API verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="3674b-167">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="3674b-168">Diese URL wird nur von der Azure-API-Verwaltung verwendet und nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="3674b-168">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="3674b-169">Die URL muss ein bis 2000 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="3674b-169">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="3674b-170">-SourceApiId</span><span class="sxs-lookup"><span data-stu-id="3674b-170">-SourceApiId</span></span>
<span data-ttu-id="3674b-171">API-Bezeichner der Quell-API.</span><span class="sxs-lookup"><span data-stu-id="3674b-171">Api identifier of the source API.</span></span> <span data-ttu-id="3674b-172">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="3674b-172">This parameter is optional.</span></span>

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

### <span data-ttu-id="3674b-173">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="3674b-173">-SourceApiRevision</span></span>
<span data-ttu-id="3674b-174">API-Revision der Quell-API.</span><span class="sxs-lookup"><span data-stu-id="3674b-174">Api Revision of the source API.</span></span> <span data-ttu-id="3674b-175">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="3674b-175">This parameter is optional.</span></span>

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

### <span data-ttu-id="3674b-176">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="3674b-176">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="3674b-177">Gibt den Namen des Abonnementschlüssel Headers an.</span><span class="sxs-lookup"><span data-stu-id="3674b-177">Specifies the subscription key header name.</span></span>
<span data-ttu-id="3674b-178">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="3674b-178">The default value is $Null.</span></span>

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

### <span data-ttu-id="3674b-179">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="3674b-179">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="3674b-180">Gibt den Abfragezeichenfolgenparameter Namen für den Abonnementschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="3674b-180">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="3674b-181">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="3674b-181">The default value is $Null.</span></span>

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

### <span data-ttu-id="3674b-182">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="3674b-182">-SubscriptionRequired</span></span>
<span data-ttu-id="3674b-183">Flag zum Erzwingen von SubscriptionRequired für Anforderungen an die API.</span><span class="sxs-lookup"><span data-stu-id="3674b-183">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="3674b-184">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="3674b-184">This parameter is optional.</span></span>

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

### <span data-ttu-id="3674b-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3674b-185">CommonParameters</span></span>
<span data-ttu-id="3674b-186">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3674b-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3674b-187">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3674b-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3674b-188">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3674b-188">INPUTS</span></span>

### <span data-ttu-id="3674b-189">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3674b-189">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3674b-190">System. String</span><span class="sxs-lookup"><span data-stu-id="3674b-190">System.String</span></span>

### <span data-ttu-id="3674b-191">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="3674b-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="3674b-192">System. String []</span><span class="sxs-lookup"><span data-stu-id="3674b-192">System.String[]</span></span>

## <span data-ttu-id="3674b-193">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3674b-193">OUTPUTS</span></span>

### <span data-ttu-id="3674b-194">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3674b-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="3674b-195">Notizen</span><span class="sxs-lookup"><span data-stu-id="3674b-195">NOTES</span></span>

## <span data-ttu-id="3674b-196">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3674b-196">RELATED LINKS</span></span>

[<span data-ttu-id="3674b-197">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3674b-197">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="3674b-198">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3674b-198">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="3674b-199">Importieren-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3674b-199">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="3674b-200">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3674b-200">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="3674b-201">Satz-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3674b-201">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


