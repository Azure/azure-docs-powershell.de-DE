---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 45B96AB0-ACE3-4754-B162-88027AC8CA41
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: cfba050b3ec6e464465d72e5f8d236f3b253fd0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498081"
---
# <span data-ttu-id="f9de6-101">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="f9de6-101">New-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="f9de6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f9de6-102">SYNOPSIS</span></span>
<span data-ttu-id="f9de6-103">Erstellt einen autorisierungsserver.</span><span class="sxs-lookup"><span data-stu-id="f9de6-103">Creates an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9de6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9de6-104">SYNTAX</span></span>

```
New-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 -Name <String> [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9de6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9de6-105">DESCRIPTION</span></span>
<span data-ttu-id="f9de6-106">Mit dem Cmdlet **New-AzureRmApiManagementAuthorizationServer** wird ein Azure API-Verwaltungs autorisierungsserver erstellt.</span><span class="sxs-lookup"><span data-stu-id="f9de6-106">The **New-AzureRmApiManagementAuthorizationServer** cmdlet creates an Azure API Management authorization server.</span></span>

## <span data-ttu-id="f9de6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9de6-107">EXAMPLES</span></span>

### <span data-ttu-id="f9de6-108">Beispiel 1: Erstellen eines autorisierungsservers</span><span class="sxs-lookup"><span data-stu-id="f9de6-108">Example 1: Create an authorization server</span></span>
```
PS C:\>New-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signup" -AuthorizationEndpointUrl "https://contoso/auth" -TokenEndpointUrl "https://contoso/token" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get', 'Post') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ResourceOwnerPassword', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'; 'par2'='val2'} -AccessTokenSendingMethods @('AuthorizationHeader', 'Query') -ResourceOwnerUsername "ivan" -ResourceOwnerPassword "qwerty"
```

<span data-ttu-id="f9de6-109">Dieser Befehl erstellt einen autorisierungsserver.</span><span class="sxs-lookup"><span data-stu-id="f9de6-109">This command creates an authorization server.</span></span>

## <span data-ttu-id="f9de6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9de6-110">PARAMETERS</span></span>

### <span data-ttu-id="f9de6-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="f9de6-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="f9de6-112">Gibt ein Array von Methoden an, um ein Zugriffstoken zu senden.</span><span class="sxs-lookup"><span data-stu-id="f9de6-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="f9de6-113">psdx_paramvalues AuthorizationHeader und Abfrage.</span><span class="sxs-lookup"><span data-stu-id="f9de6-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="f9de6-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="f9de6-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="f9de6-115">Gibt den Autorisierungs Endpunkt an, um Ressourcenbesitzer zu authentifizieren und Autorisierungs Zuschüsse zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f9de6-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="f9de6-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="f9de6-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="f9de6-117">Gibt ein Array von Autorisierungs Anforderungsmethoden an.</span><span class="sxs-lookup"><span data-stu-id="f9de6-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="f9de6-118">Gültige Werte sind: Get, Post.</span><span class="sxs-lookup"><span data-stu-id="f9de6-118">Valid values are: GET, POST.</span></span>
<span data-ttu-id="f9de6-119">Der Standardwert ist Get.</span><span class="sxs-lookup"><span data-stu-id="f9de6-119">The default value is GET.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: Get, Post

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9de6-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="f9de6-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="f9de6-121">Gibt ein Array von Clientauthentifizierungsmethoden an.</span><span class="sxs-lookup"><span data-stu-id="f9de6-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="f9de6-122">psdx_paramvalues Basic und Body.</span><span class="sxs-lookup"><span data-stu-id="f9de6-122">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="f9de6-123">-ClientID</span><span class="sxs-lookup"><span data-stu-id="f9de6-123">-ClientId</span></span>
<span data-ttu-id="f9de6-124">Gibt die Client-ID der Entwicklerkonsole an, bei der es sich um die Clientanwendung handelt.</span><span class="sxs-lookup"><span data-stu-id="f9de6-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="f9de6-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="f9de6-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="f9de6-126">Gibt den Client Registrierungs Endpunkt an, um Clients beim autorisierungsserver zu registrieren und Clientanmeldeinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f9de6-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="f9de6-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="f9de6-127">-ClientSecret</span></span>
<span data-ttu-id="f9de6-128">Gibt das Client Geheimnis der Entwicklerkonsole an, bei der es sich um die Clientanwendung handelt.</span><span class="sxs-lookup"><span data-stu-id="f9de6-128">Specifies the client secret of developer console that is the client application.</span></span>

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

### <span data-ttu-id="f9de6-129">-Context</span><span class="sxs-lookup"><span data-stu-id="f9de6-129">-Context</span></span>
<span data-ttu-id="f9de6-130">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f9de6-130">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9de6-131">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="f9de6-131">-DefaultScope</span></span>
<span data-ttu-id="f9de6-132">Gibt den Standardbereich für den autorisierungsserver an.</span><span class="sxs-lookup"><span data-stu-id="f9de6-132">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="f9de6-133">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9de6-133">-Description</span></span>
<span data-ttu-id="f9de6-134">Gibt eine Beschreibung für einen autorisierungsserver an.</span><span class="sxs-lookup"><span data-stu-id="f9de6-134">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="f9de6-135">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="f9de6-135">-GrantTypes</span></span>
<span data-ttu-id="f9de6-136">Gibt ein Array von Grant-Typen an.</span><span class="sxs-lookup"><span data-stu-id="f9de6-136">Specifies an array of grant types.</span></span>
<span data-ttu-id="f9de6-137">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="f9de6-137">psdx_paramvalues</span></span>

- <span data-ttu-id="f9de6-138">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="f9de6-138">AuthorizationCode</span></span>
- <span data-ttu-id="f9de6-139">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="f9de6-139">ClientCredentials</span></span> 
- <span data-ttu-id="f9de6-140">Implizite</span><span class="sxs-lookup"><span data-stu-id="f9de6-140">Implicit</span></span> 
- <span data-ttu-id="f9de6-141">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="f9de6-141">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="f9de6-142">-Name</span><span class="sxs-lookup"><span data-stu-id="f9de6-142">-Name</span></span>
<span data-ttu-id="f9de6-143">Gibt den Namen des zu erstellende autorisierungsservers an.</span><span class="sxs-lookup"><span data-stu-id="f9de6-143">Specifies the name of the authorization server to create.</span></span>

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

### <span data-ttu-id="f9de6-144">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="f9de6-144">-ResourceOwnerPassword</span></span>
<span data-ttu-id="f9de6-145">Gibt das Kennwort des Ressourcen Besitzers an.</span><span class="sxs-lookup"><span data-stu-id="f9de6-145">Specifies the resource owner password.</span></span>
<span data-ttu-id="f9de6-146">Sie müssen angeben, dass dieser Parameter erforderlich ist, wenn ResourceOwnerPassword durch den *GrantTypes* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f9de6-146">You must specify this parameter is required if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="f9de6-147">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="f9de6-147">-ResourceOwnerUsername</span></span>
<span data-ttu-id="f9de6-148">Gibt den Benutzernamen des Ressourcen Besitzers an.</span><span class="sxs-lookup"><span data-stu-id="f9de6-148">Specifies the resource owner user name.</span></span>
<span data-ttu-id="f9de6-149">Sie müssen diesen Parameter angeben, wenn ResourceOwnerPassword durch den *GrantTypes* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f9de6-149">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="f9de6-150">-Server-Nr</span><span class="sxs-lookup"><span data-stu-id="f9de6-150">-ServerId</span></span>
<span data-ttu-id="f9de6-151">Gibt die ID des zu erstellende autorisierungsservers an.</span><span class="sxs-lookup"><span data-stu-id="f9de6-151">Specifies the ID of the authorization server to create.</span></span>

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

### <span data-ttu-id="f9de6-152">-SupportState</span><span class="sxs-lookup"><span data-stu-id="f9de6-152">-SupportState</span></span>
<span data-ttu-id="f9de6-153">Gibt an, ob der *Zustands* Parameter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="f9de6-153">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="f9de6-154">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="f9de6-154">-TokenBodyParameters</span></span>
<span data-ttu-id="f9de6-155">Gibt zusätzliche Body-Parameter mithilfe von **Application/x-www-form-urlencoded-** Format an.</span><span class="sxs-lookup"><span data-stu-id="f9de6-155">Specifies additional body parameters using **application/x-www-form-urlencoded** format.</span></span>

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

### <span data-ttu-id="f9de6-156">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="f9de6-156">-TokenEndpointUrl</span></span>
<span data-ttu-id="f9de6-157">Gibt die Token-Endpunkt-URL an, die von Clients zum Abrufen von Zugriffstoken in Exchange zum Darstellen von Autorisierungs Zuschüssen oder Aktualisierungs Tokens verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f9de6-157">Specifies the token endpoint URL that is used by clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="f9de6-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9de6-158">-DefaultProfile</span></span>
<span data-ttu-id="f9de6-159">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f9de6-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9de6-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9de6-160">CommonParameters</span></span>
<span data-ttu-id="f9de6-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9de6-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9de6-162">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9de6-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9de6-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f9de6-163">INPUTS</span></span>

## <span data-ttu-id="f9de6-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f9de6-164">OUTPUTS</span></span>

### <span data-ttu-id="f9de6-165">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="f9de6-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="f9de6-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="f9de6-166">NOTES</span></span>

## <span data-ttu-id="f9de6-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f9de6-167">RELATED LINKS</span></span>

