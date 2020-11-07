---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 93005775-3AB9-43C5-B353-45B82124ADB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 88e7c1304aae987dbf7315d5ed474969af12ba08
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821008"
---
# <span data-ttu-id="8acc6-101">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="8acc6-101">Set-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="8acc6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8acc6-102">SYNOPSIS</span></span>
<span data-ttu-id="8acc6-103">Ändert einen autorisierungsserver.</span><span class="sxs-lookup"><span data-stu-id="8acc6-103">Modifies an authorization server.</span></span>

## <span data-ttu-id="8acc6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8acc6-104">SYNTAX</span></span>

```
Set-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> -Name <String>
 [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8acc6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8acc6-105">DESCRIPTION</span></span>
<span data-ttu-id="8acc6-106">Das Cmdlet " **Satz-AzApiManagementAuthorizationServer** " ändert die Details der Azure API-Verwaltungs autorisierungsserver.</span><span class="sxs-lookup"><span data-stu-id="8acc6-106">The **Set-AzApiManagementAuthorizationServer** cmdlet modifies Azure API Management authorization server details.</span></span>

## <span data-ttu-id="8acc6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8acc6-107">EXAMPLES</span></span>

### <span data-ttu-id="8acc6-108">Beispiel 1: Ändern eines autorisierungsservers</span><span class="sxs-lookup"><span data-stu-id="8acc6-108">Example 1: Modify an authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementAuthrizarionServer -Context $ApiMgmtContext -ServerId 0123456789 -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signupv2" -AuthorizationEndpointUrl "https://contoso/authv2" -TokenEndpointUrl "https://contoso/tokenv2" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'} -AccessTokenSendingMethods @('AuthorizationHeader')
```

<span data-ttu-id="8acc6-109">Mit diesem Befehl wird der angegebene API-Verwaltungs autorisierungsserver geändert.</span><span class="sxs-lookup"><span data-stu-id="8acc6-109">This command modifies the specified API Management authorization server.</span></span>

## <span data-ttu-id="8acc6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8acc6-110">PARAMETERS</span></span>

### <span data-ttu-id="8acc6-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="8acc6-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="8acc6-112">Gibt ein Array von Methoden an, um ein Zugriffstoken zu senden.</span><span class="sxs-lookup"><span data-stu-id="8acc6-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="8acc6-113">psdx_paramvalues AuthorizationHeader und Abfrage.</span><span class="sxs-lookup"><span data-stu-id="8acc6-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="8acc6-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="8acc6-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="8acc6-115">Gibt den Autorisierungs Endpunkt an, um Ressourcenbesitzer zu authentifizieren und Autorisierungs Zuschüsse zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8acc6-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="8acc6-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="8acc6-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="8acc6-117">Gibt ein Array von Autorisierungs Anforderungsmethoden an.</span><span class="sxs-lookup"><span data-stu-id="8acc6-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="8acc6-118">psdx_paramvalues abrufen und bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8acc6-118">psdx_paramvalues GET and POST.</span></span>
<span data-ttu-id="8acc6-119">Der Standardwert ist Get.</span><span class="sxs-lookup"><span data-stu-id="8acc6-119">The default value is GET.</span></span>

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

### <span data-ttu-id="8acc6-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="8acc6-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="8acc6-121">Gibt ein Array von Clientauthentifizierungsmethoden an.</span><span class="sxs-lookup"><span data-stu-id="8acc6-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="8acc6-122">psdx_paramvalues Basic und Body.</span><span class="sxs-lookup"><span data-stu-id="8acc6-122">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="8acc6-123">-ClientID</span><span class="sxs-lookup"><span data-stu-id="8acc6-123">-ClientId</span></span>
<span data-ttu-id="8acc6-124">Gibt die Client-ID der Entwicklerkonsole an, bei der es sich um die Clientanwendung handelt.</span><span class="sxs-lookup"><span data-stu-id="8acc6-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="8acc6-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="8acc6-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="8acc6-126">Gibt den Client Registrierungs Endpunkt an, um Clients beim autorisierungsserver zu registrieren und Clientanmeldeinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8acc6-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="8acc6-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="8acc6-127">-ClientSecret</span></span>
<span data-ttu-id="8acc6-128">Gibt den Client Schlüssel der Entwicklerkonsole an, bei der es sich um die Clientanwendung handelt.</span><span class="sxs-lookup"><span data-stu-id="8acc6-128">Specifies the client secret of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="8acc6-129">-Context</span><span class="sxs-lookup"><span data-stu-id="8acc6-129">-Context</span></span>
<span data-ttu-id="8acc6-130">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8acc6-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8acc6-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8acc6-131">-DefaultProfile</span></span>
<span data-ttu-id="8acc6-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8acc6-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8acc6-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="8acc6-133">-DefaultScope</span></span>
<span data-ttu-id="8acc6-134">Gibt den Standardbereich für den autorisierungsserver an.</span><span class="sxs-lookup"><span data-stu-id="8acc6-134">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="8acc6-135">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8acc6-135">-Description</span></span>
<span data-ttu-id="8acc6-136">Gibt eine Beschreibung für einen autorisierungsserver an.</span><span class="sxs-lookup"><span data-stu-id="8acc6-136">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="8acc6-137">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="8acc6-137">-GrantTypes</span></span>
<span data-ttu-id="8acc6-138">Gibt ein Array von Grant-Typen an.</span><span class="sxs-lookup"><span data-stu-id="8acc6-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="8acc6-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="8acc6-139">psdx_paramvalues</span></span>
- <span data-ttu-id="8acc6-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="8acc6-140">AuthorizationCode</span></span>
- <span data-ttu-id="8acc6-141">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="8acc6-141">ClientCredentials</span></span> 
- <span data-ttu-id="8acc6-142">Implizite</span><span class="sxs-lookup"><span data-stu-id="8acc6-142">Implicit</span></span> 
- <span data-ttu-id="8acc6-143">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="8acc6-143">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="8acc6-144">-Name</span><span class="sxs-lookup"><span data-stu-id="8acc6-144">-Name</span></span>
<span data-ttu-id="8acc6-145">Gibt den Namen des zu ändernden autorisierungsservers an.</span><span class="sxs-lookup"><span data-stu-id="8acc6-145">Specifies the name of the authorization server to modify.</span></span>

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

### <span data-ttu-id="8acc6-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8acc6-146">-PassThru</span></span>
<span data-ttu-id="8acc6-147">passthru</span><span class="sxs-lookup"><span data-stu-id="8acc6-147">passthru</span></span>

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

### <span data-ttu-id="8acc6-148">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="8acc6-148">-ResourceOwnerPassword</span></span>
<span data-ttu-id="8acc6-149">Gibt das Kennwort des Ressourcen Besitzers an.</span><span class="sxs-lookup"><span data-stu-id="8acc6-149">Specifies the resource owner password.</span></span>
<span data-ttu-id="8acc6-150">Sie müssen diesen Parameter angeben, wenn ResourceOwnerPassword durch den *GrantTypes* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8acc6-150">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="8acc6-151">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="8acc6-151">-ResourceOwnerUsername</span></span>
<span data-ttu-id="8acc6-152">Gibt den Benutzernamen des Ressourcen Besitzers an.</span><span class="sxs-lookup"><span data-stu-id="8acc6-152">Specifies the resource owner user name.</span></span>
<span data-ttu-id="8acc6-153">Sie müssen diesen Parameter angeben, wenn ResourceOwnerPassword durch den *GrantTypes* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8acc6-153">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="8acc6-154">-Server-Nr</span><span class="sxs-lookup"><span data-stu-id="8acc6-154">-ServerId</span></span>
<span data-ttu-id="8acc6-155">Gibt die ID des zu ändernden autorisierungsservers an.</span><span class="sxs-lookup"><span data-stu-id="8acc6-155">Specifies the ID of the authorization server to modify.</span></span>

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

### <span data-ttu-id="8acc6-156">-SupportState</span><span class="sxs-lookup"><span data-stu-id="8acc6-156">-SupportState</span></span>
<span data-ttu-id="8acc6-157">Gibt an, ob der *Zustands* Parameter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="8acc6-157">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="8acc6-158">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="8acc6-158">-TokenBodyParameters</span></span>
<span data-ttu-id="8acc6-159">Gibt zusätzliche Body-Parameter mithilfe von Application/x-www-form-urlencoded-Format an.</span><span class="sxs-lookup"><span data-stu-id="8acc6-159">Specifies additional body parameters using application/x-www-form-urlencoded format.</span></span>

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

### <span data-ttu-id="8acc6-160">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="8acc6-160">-TokenEndpointUrl</span></span>
<span data-ttu-id="8acc6-161">Gibt den Token-Endpunkt für Clients an, um in Exchange Zugriffstoken für die Darstellung von Autorisierungs Zuschüssen oder Aktualisierungstoken zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8acc6-161">Specifies the token endpoint for clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="8acc6-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8acc6-162">CommonParameters</span></span>
<span data-ttu-id="8acc6-163">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8acc6-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8acc6-164">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8acc6-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8acc6-165">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8acc6-165">INPUTS</span></span>

### <span data-ttu-id="8acc6-166">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8acc6-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8acc6-167">System. String</span><span class="sxs-lookup"><span data-stu-id="8acc6-167">System.String</span></span>

### <span data-ttu-id="8acc6-168">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementAuthorizationRequestMethod []</span><span class="sxs-lookup"><span data-stu-id="8acc6-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]</span></span>

### <span data-ttu-id="8acc6-169">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementGrantType []</span><span class="sxs-lookup"><span data-stu-id="8acc6-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]</span></span>

### <span data-ttu-id="8acc6-170">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementClientAuthenticationMethod []</span><span class="sxs-lookup"><span data-stu-id="8acc6-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]</span></span>

### <span data-ttu-id="8acc6-171">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8acc6-171">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8acc6-172">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8acc6-172">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8acc6-173">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementAccessTokenSendingMethod []</span><span class="sxs-lookup"><span data-stu-id="8acc6-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]</span></span>

### <span data-ttu-id="8acc6-174">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="8acc6-174">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8acc6-175">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8acc6-175">OUTPUTS</span></span>

### <span data-ttu-id="8acc6-176">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="8acc6-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="8acc6-177">Notizen</span><span class="sxs-lookup"><span data-stu-id="8acc6-177">NOTES</span></span>

## <span data-ttu-id="8acc6-178">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8acc6-178">RELATED LINKS</span></span>

[<span data-ttu-id="8acc6-179">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="8acc6-179">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="8acc6-180">Neu – AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="8acc6-180">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="8acc6-181">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="8acc6-181">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)


