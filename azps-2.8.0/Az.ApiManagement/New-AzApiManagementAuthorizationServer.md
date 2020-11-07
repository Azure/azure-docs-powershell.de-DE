---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 45B96AB0-ACE3-4754-B162-88027AC8CA41
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: f6e71bd6fe7d77e083b43c3b36e7660b1f38d713
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658271"
---
# <span data-ttu-id="0a613-101">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="0a613-101">New-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="0a613-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0a613-102">SYNOPSIS</span></span>
<span data-ttu-id="0a613-103">Erstellt einen autorisierungsserver.</span><span class="sxs-lookup"><span data-stu-id="0a613-103">Creates an authorization server.</span></span>

## <span data-ttu-id="0a613-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a613-104">SYNTAX</span></span>

```
New-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>] -Name <String>
 [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a613-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a613-105">DESCRIPTION</span></span>
<span data-ttu-id="0a613-106">Mit dem Cmdlet **New-AzApiManagementAuthorizationServer** wird ein Azure API-Verwaltungs autorisierungsserver erstellt.</span><span class="sxs-lookup"><span data-stu-id="0a613-106">The **New-AzApiManagementAuthorizationServer** cmdlet creates an Azure API Management authorization server.</span></span>

## <span data-ttu-id="0a613-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a613-107">EXAMPLES</span></span>

### <span data-ttu-id="0a613-108">Beispiel 1: Erstellen eines autorisierungsservers</span><span class="sxs-lookup"><span data-stu-id="0a613-108">Example 1: Create an authorization server</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signup" -AuthorizationEndpointUrl "https://contoso/auth" -TokenEndpointUrl "https://contoso/token" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get', 'Post') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ResourceOwnerPassword', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'; 'par2'='val2'} -AccessTokenSendingMethods @('AuthorizationHeader', 'Query') -ResourceOwnerUsername "ivan" -ResourceOwnerPassword "qwerty"
```

<span data-ttu-id="0a613-109">Dieser Befehl erstellt einen autorisierungsserver.</span><span class="sxs-lookup"><span data-stu-id="0a613-109">This command creates an authorization server.</span></span>

## <span data-ttu-id="0a613-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a613-110">PARAMETERS</span></span>

### <span data-ttu-id="0a613-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="0a613-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="0a613-112">Gibt ein Array von Methoden an, um ein Zugriffstoken zu senden.</span><span class="sxs-lookup"><span data-stu-id="0a613-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="0a613-113">psdx_paramvalues AuthorizationHeader und Abfrage.</span><span class="sxs-lookup"><span data-stu-id="0a613-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: AuthorizationHeader, Query

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a613-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="0a613-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="0a613-115">Gibt den Autorisierungs Endpunkt an, um Ressourcenbesitzer zu authentifizieren und Autorisierungs Zuschüsse zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0a613-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="0a613-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="0a613-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="0a613-117">Gibt ein Array von Autorisierungs Anforderungsmethoden an.</span><span class="sxs-lookup"><span data-stu-id="0a613-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="0a613-118">Gültige Werte sind: Get, Post.</span><span class="sxs-lookup"><span data-stu-id="0a613-118">Valid values are: GET, POST.</span></span>
<span data-ttu-id="0a613-119">Der Standardwert ist Get.</span><span class="sxs-lookup"><span data-stu-id="0a613-119">The default value is GET.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: Get, Post, Head, Options, Trace, Put, Patch, Delete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a613-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="0a613-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="0a613-121">Gibt ein Array von Clientauthentifizierungsmethoden an.</span><span class="sxs-lookup"><span data-stu-id="0a613-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="0a613-122">psdx_paramvalues Basic und Body.</span><span class="sxs-lookup"><span data-stu-id="0a613-122">psdx_paramvalues Basic and Body.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Body

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a613-123">-ClientID</span><span class="sxs-lookup"><span data-stu-id="0a613-123">-ClientId</span></span>
<span data-ttu-id="0a613-124">Gibt die Client-ID der Entwicklerkonsole an, bei der es sich um die Clientanwendung handelt.</span><span class="sxs-lookup"><span data-stu-id="0a613-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="0a613-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="0a613-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="0a613-126">Gibt den Client Registrierungs Endpunkt an, um Clients beim autorisierungsserver zu registrieren und Clientanmeldeinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0a613-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="0a613-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="0a613-127">-ClientSecret</span></span>
<span data-ttu-id="0a613-128">Gibt das Client Geheimnis der Entwicklerkonsole an, bei der es sich um die Clientanwendung handelt.</span><span class="sxs-lookup"><span data-stu-id="0a613-128">Specifies the client secret of developer console that is the client application.</span></span>

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

### <span data-ttu-id="0a613-129">-Context</span><span class="sxs-lookup"><span data-stu-id="0a613-129">-Context</span></span>
<span data-ttu-id="0a613-130">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="0a613-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0a613-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a613-131">-DefaultProfile</span></span>
<span data-ttu-id="0a613-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0a613-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a613-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="0a613-133">-DefaultScope</span></span>
<span data-ttu-id="0a613-134">Gibt den Standardbereich für den autorisierungsserver an.</span><span class="sxs-lookup"><span data-stu-id="0a613-134">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="0a613-135">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a613-135">-Description</span></span>
<span data-ttu-id="0a613-136">Gibt eine Beschreibung für einen autorisierungsserver an.</span><span class="sxs-lookup"><span data-stu-id="0a613-136">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="0a613-137">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="0a613-137">-GrantTypes</span></span>
<span data-ttu-id="0a613-138">Gibt ein Array von Grant-Typen an.</span><span class="sxs-lookup"><span data-stu-id="0a613-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="0a613-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="0a613-139">psdx_paramvalues</span></span>
- <span data-ttu-id="0a613-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="0a613-140">AuthorizationCode</span></span>
- <span data-ttu-id="0a613-141">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="0a613-141">ClientCredentials</span></span> 
- <span data-ttu-id="0a613-142">Implizite</span><span class="sxs-lookup"><span data-stu-id="0a613-142">Implicit</span></span> 
- <span data-ttu-id="0a613-143">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="0a613-143">ResourceOwnerPassword</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]
Parameter Sets: (All)
Aliases:
Accepted values: AuthorizationCode, Implicit, ResourceOwnerPassword, ClientCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a613-144">-Name</span><span class="sxs-lookup"><span data-stu-id="0a613-144">-Name</span></span>
<span data-ttu-id="0a613-145">Gibt den Namen des zu erstellende autorisierungsservers an.</span><span class="sxs-lookup"><span data-stu-id="0a613-145">Specifies the name of the authorization server to create.</span></span>

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

### <span data-ttu-id="0a613-146">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="0a613-146">-ResourceOwnerPassword</span></span>
<span data-ttu-id="0a613-147">Gibt das Kennwort des Ressourcen Besitzers an.</span><span class="sxs-lookup"><span data-stu-id="0a613-147">Specifies the resource owner password.</span></span>
<span data-ttu-id="0a613-148">Sie müssen angeben, dass dieser Parameter erforderlich ist, wenn ResourceOwnerPassword durch den *GrantTypes* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0a613-148">You must specify this parameter is required if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="0a613-149">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="0a613-149">-ResourceOwnerUsername</span></span>
<span data-ttu-id="0a613-150">Gibt den Benutzernamen des Ressourcen Besitzers an.</span><span class="sxs-lookup"><span data-stu-id="0a613-150">Specifies the resource owner user name.</span></span>
<span data-ttu-id="0a613-151">Sie müssen diesen Parameter angeben, wenn ResourceOwnerPassword durch den *GrantTypes* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0a613-151">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="0a613-152">-Server-Nr</span><span class="sxs-lookup"><span data-stu-id="0a613-152">-ServerId</span></span>
<span data-ttu-id="0a613-153">Gibt die ID des zu erstellende autorisierungsservers an.</span><span class="sxs-lookup"><span data-stu-id="0a613-153">Specifies the ID of the authorization server to create.</span></span>

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

### <span data-ttu-id="0a613-154">-SupportState</span><span class="sxs-lookup"><span data-stu-id="0a613-154">-SupportState</span></span>
<span data-ttu-id="0a613-155">Gibt an, ob der *Zustands* Parameter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="0a613-155">Indicates whether to support the *State* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a613-156">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="0a613-156">-TokenBodyParameters</span></span>
<span data-ttu-id="0a613-157">Gibt zusätzliche Body-Parameter mithilfe von **Application/x-www-form-urlencoded-** Format an.</span><span class="sxs-lookup"><span data-stu-id="0a613-157">Specifies additional body parameters using **application/x-www-form-urlencoded** format.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a613-158">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="0a613-158">-TokenEndpointUrl</span></span>
<span data-ttu-id="0a613-159">Gibt die Token-Endpunkt-URL an, die von Clients zum Abrufen von Zugriffstoken in Exchange zum Darstellen von Autorisierungs Zuschüssen oder Aktualisierungs Tokens verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0a613-159">Specifies the token endpoint URL that is used by clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="0a613-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a613-160">CommonParameters</span></span>
<span data-ttu-id="0a613-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a613-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a613-162">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a613-162">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a613-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0a613-163">INPUTS</span></span>

### <span data-ttu-id="0a613-164">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0a613-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0a613-165">System. String</span><span class="sxs-lookup"><span data-stu-id="0a613-165">System.String</span></span>

### <span data-ttu-id="0a613-166">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementAuthorizationRequestMethod []</span><span class="sxs-lookup"><span data-stu-id="0a613-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]</span></span>

### <span data-ttu-id="0a613-167">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementGrantType []</span><span class="sxs-lookup"><span data-stu-id="0a613-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]</span></span>

### <span data-ttu-id="0a613-168">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementClientAuthenticationMethod []</span><span class="sxs-lookup"><span data-stu-id="0a613-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]</span></span>

### <span data-ttu-id="0a613-169">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0a613-169">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0a613-170">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0a613-170">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0a613-171">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementAccessTokenSendingMethod []</span><span class="sxs-lookup"><span data-stu-id="0a613-171">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]</span></span>

## <span data-ttu-id="0a613-172">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0a613-172">OUTPUTS</span></span>

### <span data-ttu-id="0a613-173">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="0a613-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="0a613-174">Notizen</span><span class="sxs-lookup"><span data-stu-id="0a613-174">NOTES</span></span>

## <span data-ttu-id="0a613-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0a613-175">RELATED LINKS</span></span>
