---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 93005775-3AB9-43C5-B353-45B82124ADB7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 6424ad453d7e2ee3c4933127cc58e6d3e1193e76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503125"
---
# <span data-ttu-id="5b85f-101">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="5b85f-101">Set-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="5b85f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5b85f-102">SYNOPSIS</span></span>
<span data-ttu-id="5b85f-103">Ändert einen autorisierungsserver.</span><span class="sxs-lookup"><span data-stu-id="5b85f-103">Modifies an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b85f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b85f-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> -Name <String>
 [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b85f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b85f-105">DESCRIPTION</span></span>
<span data-ttu-id="5b85f-106">Das Cmdlet " **Satz-AzureRmApiManagementAuthorizationServer** " ändert die Details der Azure API-Verwaltungs autorisierungsserver.</span><span class="sxs-lookup"><span data-stu-id="5b85f-106">The **Set-AzureRmApiManagementAuthorizationServer** cmdlet modifies Azure API Management authorization server details.</span></span>

## <span data-ttu-id="5b85f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b85f-107">EXAMPLES</span></span>

### <span data-ttu-id="5b85f-108">Beispiel 1: Ändern eines autorisierungsservers</span><span class="sxs-lookup"><span data-stu-id="5b85f-108">Example 1: Modify an authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext -ServerId 0123456789 -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signupv2" -AuthorizationEndpointUrl "https://contoso/authv2" -TokenEndpointUrl "https://contoso/tokenv2" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'} -AccessTokenSendingMethods @('AuthorizationHeader')
```

<span data-ttu-id="5b85f-109">Mit diesem Befehl wird der angegebene API-Verwaltungs autorisierungsserver geändert.</span><span class="sxs-lookup"><span data-stu-id="5b85f-109">This command modifies the specified API Management authorization server.</span></span>

## <span data-ttu-id="5b85f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b85f-110">PARAMETERS</span></span>

### <span data-ttu-id="5b85f-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="5b85f-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="5b85f-112">Gibt ein Array von Methoden an, um ein Zugriffstoken zu senden.</span><span class="sxs-lookup"><span data-stu-id="5b85f-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="5b85f-113">psdx_paramvalues AuthorizationHeader und Abfrage.</span><span class="sxs-lookup"><span data-stu-id="5b85f-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

```yaml
Type: PsApiManagementAccessTokenSendingMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: AuthorizationHeader, Query

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b85f-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="5b85f-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="5b85f-115">Gibt den Autorisierungs Endpunkt an, um Ressourcenbesitzer zu authentifizieren und Autorisierungs Zuschüsse zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5b85f-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b85f-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="5b85f-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="5b85f-117">Gibt ein Array von Autorisierungs Anforderungsmethoden an.</span><span class="sxs-lookup"><span data-stu-id="5b85f-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="5b85f-118">psdx_paramvalues abrufen und bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5b85f-118">psdx_paramvalues GET and POST.</span></span>
<span data-ttu-id="5b85f-119">Der Standardwert ist Get.</span><span class="sxs-lookup"><span data-stu-id="5b85f-119">The default value is GET.</span></span>

```yaml
Type: PsApiManagementAuthorizationRequestMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: Get, Post

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b85f-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="5b85f-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="5b85f-121">Gibt ein Array von Clientauthentifizierungsmethoden an.</span><span class="sxs-lookup"><span data-stu-id="5b85f-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="5b85f-122">psdx_paramvalues Basic und Body.</span><span class="sxs-lookup"><span data-stu-id="5b85f-122">psdx_paramvalues Basic and Body.</span></span>

```yaml
Type: PsApiManagementClientAuthenticationMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Body

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b85f-123">-ClientID</span><span class="sxs-lookup"><span data-stu-id="5b85f-123">-ClientId</span></span>
<span data-ttu-id="5b85f-124">Gibt die Client-ID der Entwicklerkonsole an, bei der es sich um die Clientanwendung handelt.</span><span class="sxs-lookup"><span data-stu-id="5b85f-124">Specifies the client ID of the developer console that is the client application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b85f-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="5b85f-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="5b85f-126">Gibt den Client Registrierungs Endpunkt an, um Clients beim autorisierungsserver zu registrieren und Clientanmeldeinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5b85f-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b85f-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="5b85f-127">-ClientSecret</span></span>
<span data-ttu-id="5b85f-128">Gibt den Client Schlüssel der Entwicklerkonsole an, bei der es sich um die Clientanwendung handelt.</span><span class="sxs-lookup"><span data-stu-id="5b85f-128">Specifies the client secret of the developer console that is the client application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b85f-129">-Context</span><span class="sxs-lookup"><span data-stu-id="5b85f-129">-Context</span></span>
<span data-ttu-id="5b85f-130">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="5b85f-130">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b85f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b85f-131">-DefaultProfile</span></span>
<span data-ttu-id="5b85f-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5b85f-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b85f-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="5b85f-133">-DefaultScope</span></span>
<span data-ttu-id="5b85f-134">Gibt den Standardbereich für den autorisierungsserver an.</span><span class="sxs-lookup"><span data-stu-id="5b85f-134">Specifies the default scope for the authorization server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b85f-135">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b85f-135">-Description</span></span>
<span data-ttu-id="5b85f-136">Gibt eine Beschreibung für einen autorisierungsserver an.</span><span class="sxs-lookup"><span data-stu-id="5b85f-136">Specifies a description for an authorization server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b85f-137">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="5b85f-137">-GrantTypes</span></span>
<span data-ttu-id="5b85f-138">Gibt ein Array von Grant-Typen an.</span><span class="sxs-lookup"><span data-stu-id="5b85f-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="5b85f-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="5b85f-139">psdx_paramvalues</span></span>

- <span data-ttu-id="5b85f-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="5b85f-140">AuthorizationCode</span></span>
- <span data-ttu-id="5b85f-141">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="5b85f-141">ClientCredentials</span></span> 
- <span data-ttu-id="5b85f-142">Implizite</span><span class="sxs-lookup"><span data-stu-id="5b85f-142">Implicit</span></span> 
- <span data-ttu-id="5b85f-143">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="5b85f-143">ResourceOwnerPassword</span></span>

```yaml
Type: PsApiManagementGrantType[]
Parameter Sets: (All)
Aliases: 
Accepted values: AuthorizationCode, Implicit, ResourceOwnerPassword, ClientCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b85f-144">-Name</span><span class="sxs-lookup"><span data-stu-id="5b85f-144">-Name</span></span>
<span data-ttu-id="5b85f-145">Gibt den Namen des zu ändernden autorisierungsservers an.</span><span class="sxs-lookup"><span data-stu-id="5b85f-145">Specifies the name of the authorization server to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b85f-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b85f-146">-PassThru</span></span>
<span data-ttu-id="5b85f-147">passthru</span><span class="sxs-lookup"><span data-stu-id="5b85f-147">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b85f-148">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="5b85f-148">-ResourceOwnerPassword</span></span>
<span data-ttu-id="5b85f-149">Gibt das Kennwort des Ressourcen Besitzers an.</span><span class="sxs-lookup"><span data-stu-id="5b85f-149">Specifies the resource owner password.</span></span>
<span data-ttu-id="5b85f-150">Sie müssen diesen Parameter angeben, wenn ResourceOwnerPassword durch den *GrantTypes* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5b85f-150">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b85f-151">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="5b85f-151">-ResourceOwnerUsername</span></span>
<span data-ttu-id="5b85f-152">Gibt den Benutzernamen des Ressourcen Besitzers an.</span><span class="sxs-lookup"><span data-stu-id="5b85f-152">Specifies the resource owner user name.</span></span>
<span data-ttu-id="5b85f-153">Sie müssen diesen Parameter angeben, wenn ResourceOwnerPassword durch den *GrantTypes* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5b85f-153">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b85f-154">-Server-Nr</span><span class="sxs-lookup"><span data-stu-id="5b85f-154">-ServerId</span></span>
<span data-ttu-id="5b85f-155">Gibt die ID des zu ändernden autorisierungsservers an.</span><span class="sxs-lookup"><span data-stu-id="5b85f-155">Specifies the ID of the authorization server to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b85f-156">-SupportState</span><span class="sxs-lookup"><span data-stu-id="5b85f-156">-SupportState</span></span>
<span data-ttu-id="5b85f-157">Gibt an, ob der *Zustands* Parameter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="5b85f-157">Indicates whether to support the *State* parameter.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b85f-158">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="5b85f-158">-TokenBodyParameters</span></span>
<span data-ttu-id="5b85f-159">Gibt zusätzliche Body-Parameter mithilfe von Application/x-www-form-urlencoded-Format an.</span><span class="sxs-lookup"><span data-stu-id="5b85f-159">Specifies additional body parameters using application/x-www-form-urlencoded format.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b85f-160">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="5b85f-160">-TokenEndpointUrl</span></span>
<span data-ttu-id="5b85f-161">Gibt den Token-Endpunkt für Clients an, um in Exchange Zugriffstoken für die Darstellung von Autorisierungs Zuschüssen oder Aktualisierungstoken zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5b85f-161">Specifies the token endpoint for clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b85f-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b85f-162">CommonParameters</span></span>
<span data-ttu-id="5b85f-163">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b85f-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b85f-164">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b85f-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b85f-165">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5b85f-165">INPUTS</span></span>

### <span data-ttu-id="5b85f-166">Keine</span><span class="sxs-lookup"><span data-stu-id="5b85f-166">None</span></span>
<span data-ttu-id="5b85f-167">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="5b85f-167">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5b85f-168">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5b85f-168">OUTPUTS</span></span>

### <span data-ttu-id="5b85f-169">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="5b85f-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="5b85f-170">Notizen</span><span class="sxs-lookup"><span data-stu-id="5b85f-170">NOTES</span></span>

## <span data-ttu-id="5b85f-171">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5b85f-171">RELATED LINKS</span></span>

[<span data-ttu-id="5b85f-172">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="5b85f-172">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="5b85f-173">Neu – AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="5b85f-173">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="5b85f-174">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="5b85f-174">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)


