---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: 3312c725d63bcb42aab7d82144c5a8f6f8e67641
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168545"
---
# <span data-ttu-id="6f226-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6f226-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="6f226-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f226-102">SYNOPSIS</span></span>
<span data-ttu-id="6f226-103">Erstellt eine API.</span><span class="sxs-lookup"><span data-stu-id="6f226-103">Creates an API.</span></span>

## <span data-ttu-id="6f226-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f226-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-SubscriptionRequired]
 [-ApiVersionDescription <String>] [-ApiVersionSetId <String>] [-ApiVersion <String>] [-SourceApiId <String>]
 [-SourceApiRevision <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f226-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f226-105">DESCRIPTION</span></span>
<span data-ttu-id="6f226-106">Das **Cmdlet "New-AzApiManagementApi"** erstellt eine Azure API Management API.</span><span class="sxs-lookup"><span data-stu-id="6f226-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="6f226-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6f226-107">EXAMPLES</span></span>

### <span data-ttu-id="6f226-108">Beispiel 1: Erstellen einer API</span><span class="sxs-lookup"><span data-stu-id="6f226-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="6f226-109">Mit diesem Befehl wird eine API namens "EchoApi" mit der angegebenen URL erstellt.</span><span class="sxs-lookup"><span data-stu-id="6f226-109">This command creates an API named EchoApi with the specified URL.</span></span>

### <span data-ttu-id="6f226-110">Beispiel 2: Erstellen einer API durch Kopieren aller Operation, Tags, Produkte und Richtlinien aus der Echo-API in ein ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="6f226-110">Example 2: Create an API by copying all operation, Tags, Products and Policies from echo-api and into an ApiVersionSet</span></span>
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

<span data-ttu-id="6f226-111">Dieser Befehl erstellt eine API in ApiVersionSet und kopiert alle Operation, Tags und `echoapiv3` Richtlinien aus der `xmsVersionSet` Quell-API. `echo-api`</span><span class="sxs-lookup"><span data-stu-id="6f226-111">This command creates an API `echoapiv3` in ApiVersionSet `xmsVersionSet` and copies all operation, Tags and Policies from source Api `echo-api`.</span></span> <span data-ttu-id="6f226-112">Sie setzt "SubscriptionRequired", "ServiceUrl", "Path", "Protocols" außer Kraft</span><span class="sxs-lookup"><span data-stu-id="6f226-112">It overrides the SubscriptionRequired, ServiceUrl, Path, Protocols</span></span>

### <span data-ttu-id="6f226-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="6f226-113">Example 3</span></span>

<span data-ttu-id="6f226-114">Erstellt eine API.</span><span class="sxs-lookup"><span data-stu-id="6f226-114">Creates an API.</span></span> <span data-ttu-id="6f226-115">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="6f226-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzApiManagementApi -ApiId '0001' -Context <PsApiManagementContext> -Name 'Echo api' -Path 'echov3' -Protocols Http -ServiceUrl 'https://contoso.com/apis/echo'
```

## <span data-ttu-id="6f226-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f226-116">PARAMETERS</span></span>

### <span data-ttu-id="6f226-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6f226-117">-ApiId</span></span>
<span data-ttu-id="6f226-118">Gibt die ID der zu erstellenden API an.</span><span class="sxs-lookup"><span data-stu-id="6f226-118">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="6f226-119">Wenn Sie diesen Parameter nicht angeben, generiert dieses Cmdlet eine ID für Sie.</span><span class="sxs-lookup"><span data-stu-id="6f226-119">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="6f226-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6f226-120">-ApiVersion</span></span>
<span data-ttu-id="6f226-121">Die API-Version der zu erstellende API.</span><span class="sxs-lookup"><span data-stu-id="6f226-121">Api Version of the Api to create.</span></span> <span data-ttu-id="6f226-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6f226-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="6f226-123">-ApiVersionDescription</span><span class="sxs-lookup"><span data-stu-id="6f226-123">-ApiVersionDescription</span></span>
<span data-ttu-id="6f226-124">Api-Versionsbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="6f226-124">Api Version Description.</span></span> <span data-ttu-id="6f226-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6f226-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="6f226-126">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="6f226-126">-ApiVersionSetId</span></span>
<span data-ttu-id="6f226-127">Ein Ressourcenbezeichner für den zugehörigen API-Versionssatz.</span><span class="sxs-lookup"><span data-stu-id="6f226-127">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="6f226-128">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6f226-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="6f226-129">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="6f226-129">-AuthorizationScope</span></span>
<span data-ttu-id="6f226-130">Gibt den Bereich der OAuth-Vorgänge an.</span><span class="sxs-lookup"><span data-stu-id="6f226-130">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="6f226-131">Der Standardwert ist $Null.</span><span class="sxs-lookup"><span data-stu-id="6f226-131">The default value is $Null.</span></span>

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

### <span data-ttu-id="6f226-132">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="6f226-132">-AuthorizationServerId</span></span>
<span data-ttu-id="6f226-133">Gibt die OAuth-Autorisierungsserver-ID an.</span><span class="sxs-lookup"><span data-stu-id="6f226-133">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="6f226-134">Der Standardwert ist $Null.</span><span class="sxs-lookup"><span data-stu-id="6f226-134">The default value is $Null.</span></span>
<span data-ttu-id="6f226-135">Sie müssen diesen Parameter angeben, wenn *AuthorizationScope* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="6f226-135">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="6f226-136">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="6f226-136">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="6f226-137">OpenId authorization server mechanism by which access token is passed to the API.</span><span class="sxs-lookup"><span data-stu-id="6f226-137">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="6f226-138">Weitere Informationen finden Sie unter http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="6f226-138">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="6f226-139">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6f226-139">This parameter is optional.</span></span> <span data-ttu-id="6f226-140">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="6f226-140">Default value is $null.</span></span>

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

### <span data-ttu-id="6f226-141">-Context</span><span class="sxs-lookup"><span data-stu-id="6f226-141">-Context</span></span>
<span data-ttu-id="6f226-142">Gibt ein **"PsApiManagementContext"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="6f226-142">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6f226-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f226-143">-DefaultProfile</span></span>
<span data-ttu-id="6f226-144">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6f226-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f226-145">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6f226-145">-Description</span></span>
<span data-ttu-id="6f226-146">Gibt eine Beschreibung für die Web-API an.</span><span class="sxs-lookup"><span data-stu-id="6f226-146">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="6f226-147">-Name</span><span class="sxs-lookup"><span data-stu-id="6f226-147">-Name</span></span>
<span data-ttu-id="6f226-148">Gibt den Namen der Web-API an.</span><span class="sxs-lookup"><span data-stu-id="6f226-148">Specifies the name of the web API.</span></span>
<span data-ttu-id="6f226-149">Dies ist der öffentliche Name der API, wie sie auf den Entwickler- und Administratorportalen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6f226-149">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="6f226-150">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="6f226-150">-OpenIdProviderId</span></span>
<span data-ttu-id="6f226-151">OpenId-Autorisierungsserver-ID.</span><span class="sxs-lookup"><span data-stu-id="6f226-151">OpenId authorization server identifier.</span></span> <span data-ttu-id="6f226-152">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6f226-152">This parameter is optional.</span></span> <span data-ttu-id="6f226-153">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="6f226-153">Default value is $null.</span></span> <span data-ttu-id="6f226-154">Muss angegeben werden, wenn BearerTokenSendingMethods angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="6f226-154">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="6f226-155">-Path</span><span class="sxs-lookup"><span data-stu-id="6f226-155">-Path</span></span>
<span data-ttu-id="6f226-156">Gibt den Web-API-Pfad an, der den letzten Teil der öffentlichen URL der API angibt und dem Feld für das Suffix "Web-API-URL" im Verwaltungsportal entspricht.</span><span class="sxs-lookup"><span data-stu-id="6f226-156">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="6f226-157">Diese URL wird von Api-Kunden zum Senden von Anforderungen an den Webdienst verwendet und muss 1 bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="6f226-157">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="6f226-158">Der Standardwert ist $Null.</span><span class="sxs-lookup"><span data-stu-id="6f226-158">The default value is $Null.</span></span>

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

### <span data-ttu-id="6f226-159">-ProductIds</span><span class="sxs-lookup"><span data-stu-id="6f226-159">-ProductIds</span></span>
<span data-ttu-id="6f226-160">Gibt ein Array von Produkt-IDs an, dem die neue API hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6f226-160">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="6f226-161">-Protocols</span><span class="sxs-lookup"><span data-stu-id="6f226-161">-Protocols</span></span>
<span data-ttu-id="6f226-162">Gibt ein Array von Web-API-Protokollen an.</span><span class="sxs-lookup"><span data-stu-id="6f226-162">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="6f226-163">Gültige Werte sind "http", "https".</span><span class="sxs-lookup"><span data-stu-id="6f226-163">Valid values are http, https.</span></span>
<span data-ttu-id="6f226-164">Dies sind die Webprotokolle, über die die API verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="6f226-164">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="6f226-165">Der Standardwert ist $Null.</span><span class="sxs-lookup"><span data-stu-id="6f226-165">The default value is $Null.</span></span>

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

### <span data-ttu-id="6f226-166">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="6f226-166">-ServiceUrl</span></span>
<span data-ttu-id="6f226-167">Gibt die URL des Webdiensts an, der die API verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="6f226-167">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="6f226-168">Diese URL wird nur von Azure API Management verwendet und nicht öffentlich gemacht.</span><span class="sxs-lookup"><span data-stu-id="6f226-168">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="6f226-169">Die URL muss 1 bis 2.000 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="6f226-169">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="6f226-170">-SourceApiId</span><span class="sxs-lookup"><span data-stu-id="6f226-170">-SourceApiId</span></span>
<span data-ttu-id="6f226-171">Der API-Bezeichner der Quell-API.</span><span class="sxs-lookup"><span data-stu-id="6f226-171">Api identifier of the source API.</span></span> <span data-ttu-id="6f226-172">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6f226-172">This parameter is optional.</span></span>

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

### <span data-ttu-id="6f226-173">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="6f226-173">-SourceApiRevision</span></span>
<span data-ttu-id="6f226-174">Api-Revision der Quell-API.</span><span class="sxs-lookup"><span data-stu-id="6f226-174">Api Revision of the source API.</span></span> <span data-ttu-id="6f226-175">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6f226-175">This parameter is optional.</span></span>

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

### <span data-ttu-id="6f226-176">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="6f226-176">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="6f226-177">Gibt den Kopfzeilennamen des Abonnementschlüssels an.</span><span class="sxs-lookup"><span data-stu-id="6f226-177">Specifies the subscription key header name.</span></span>
<span data-ttu-id="6f226-178">Der Standardwert ist $Null.</span><span class="sxs-lookup"><span data-stu-id="6f226-178">The default value is $Null.</span></span>

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

### <span data-ttu-id="6f226-179">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="6f226-179">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="6f226-180">Gibt den Parameternamen der Abfragezeichenfolge des Abonnementschlüssels an.</span><span class="sxs-lookup"><span data-stu-id="6f226-180">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="6f226-181">Der Standardwert ist $Null.</span><span class="sxs-lookup"><span data-stu-id="6f226-181">The default value is $Null.</span></span>

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

### <span data-ttu-id="6f226-182">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="6f226-182">-SubscriptionRequired</span></span>
<span data-ttu-id="6f226-183">Flag zum Erzwingen von "SubscriptionRequired" für Anforderungen an die API.</span><span class="sxs-lookup"><span data-stu-id="6f226-183">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="6f226-184">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6f226-184">This parameter is optional.</span></span>

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

### <span data-ttu-id="6f226-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f226-185">CommonParameters</span></span>
<span data-ttu-id="6f226-186">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f226-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f226-187">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f226-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f226-188">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6f226-188">INPUTS</span></span>

### <span data-ttu-id="6f226-189">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6f226-189">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6f226-190">System.String</span><span class="sxs-lookup"><span data-stu-id="6f226-190">System.String</span></span>

### <span data-ttu-id="6f226-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span><span class="sxs-lookup"><span data-stu-id="6f226-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="6f226-192">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6f226-192">System.String[]</span></span>

## <span data-ttu-id="6f226-193">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6f226-193">OUTPUTS</span></span>

### <span data-ttu-id="6f226-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6f226-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="6f226-195">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6f226-195">NOTES</span></span>

## <span data-ttu-id="6f226-196">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6f226-196">RELATED LINKS</span></span>

[<span data-ttu-id="6f226-197">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6f226-197">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="6f226-198">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6f226-198">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="6f226-199">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6f226-199">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="6f226-200">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6f226-200">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="6f226-201">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6f226-201">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


