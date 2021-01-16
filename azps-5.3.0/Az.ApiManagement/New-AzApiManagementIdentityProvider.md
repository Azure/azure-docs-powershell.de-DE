---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 75f6b7cee1517a3f9ae363a7e28df420e18d37ab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382540"
---
# <span data-ttu-id="bcc09-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="bcc09-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="bcc09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcc09-102">SYNOPSIS</span></span>
<span data-ttu-id="bcc09-103">Erstellt eine neue Konfiguration des Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="bcc09-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="bcc09-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bcc09-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-SigninTenant <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcc09-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bcc09-105">DESCRIPTION</span></span>
<span data-ttu-id="bcc09-106">Erstellt eine neue Konfiguration des Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="bcc09-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="bcc09-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bcc09-107">EXAMPLES</span></span>

### <span data-ttu-id="bcc09-108">Beispiel 1: Konfigurieren von Facebook als Identitätsanbieter für Entwicklerportalanmeldungen</span><span class="sxs-lookup"><span data-stu-id="bcc09-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="bcc09-109">Mit diesem Befehl wird die Facebook-Identität im Entwicklerportal des Diensts ApiManagement als akzeptierter Identitätsanbieter konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="bcc09-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="bcc09-110">Dazu werden die ClientId und ClientSecret der Facebook-App eingegeben.</span><span class="sxs-lookup"><span data-stu-id="bcc09-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

### <span data-ttu-id="bcc09-111">Beispiel 2: Konfigurieren von adB2C als Identitätsanbieter für Entwicklerportalanmeldungen</span><span class="sxs-lookup"><span data-stu-id="bcc09-111">Example 2: Configures adB2C as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $context -Type AadB2C -ClientId 6b1fc750-9e68-450c-97d2-ba6acd0fbc20 -ClientSecret "foobar" -AllowedTenants 'samirtestbc.onmicrosoft.com' -SignupPolicyName B2C_1_signup-policy

Type                     : AadB2C
ClientId                 : 6b1fc750-9e68-450c-97d2-ba6acd0fbc20
ClientSecret             : foobar
AllowedTenants           : {samirtestbc.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         : B2C_1_signup-policy
SigninPolicyName         :
ProfileEditingPolicyName :
PasswordResetPolicyName  :
Id                       : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/identityProviders/AadB2C
ResourceGroupName        : Api-Default-WestUS
ServiceName              : contoso
```

<span data-ttu-id="bcc09-112">Mit diesem Befehl wird die Facebook-Identität im Entwicklerportal des Diensts ApiManagement als akzeptierter Identitätsanbieter konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="bcc09-112">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="bcc09-113">Dies wird als Eingabe der ClientId und des ClientSecret der Facebook-App verwendet.</span><span class="sxs-lookup"><span data-stu-id="bcc09-113">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="bcc09-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcc09-114">PARAMETERS</span></span>

### <span data-ttu-id="bcc09-115">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="bcc09-115">-AllowedTenants</span></span>
<span data-ttu-id="bcc09-116">Liste der zulässigen Azure Active Directory-Mandanten</span><span class="sxs-lookup"><span data-stu-id="bcc09-116">List of allowed Azure Active Directory Tenants</span></span>

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

### <span data-ttu-id="bcc09-117">-Authority</span><span class="sxs-lookup"><span data-stu-id="bcc09-117">-Authority</span></span>
<span data-ttu-id="bcc09-118">Hostname des OpenID Connect Discovery-Endpunkts für AAD oder AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="bcc09-118">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="bcc09-119">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="bcc09-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="bcc09-120">-ClientId</span><span class="sxs-lookup"><span data-stu-id="bcc09-120">-ClientId</span></span>
<span data-ttu-id="bcc09-121">Client-ID der Anwendung im externen Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="bcc09-121">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="bcc09-122">Es handelt sich um die App-ID für Facebook-Anmeldung, Client-ID für Google-Anmeldung, App-ID für Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bcc09-122">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="bcc09-123">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="bcc09-123">-ClientSecret</span></span>
<span data-ttu-id="bcc09-124">Der geheime Clientgeheimnis der Anwendung im externen Identitätsanbieter, der zum Authentifizieren der Anmeldeanforderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bcc09-124">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="bcc09-125">Es ist z. B. "App Secret" für die Facebook-Anmeldung, der API-Schlüssel für die Google-Anmeldung, der öffentliche Schlüssel für Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bcc09-125">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="bcc09-126">-Context</span><span class="sxs-lookup"><span data-stu-id="bcc09-126">-Context</span></span>
<span data-ttu-id="bcc09-127">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="bcc09-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="bcc09-128">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bcc09-128">This parameter is required.</span></span>

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

### <span data-ttu-id="bcc09-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcc09-129">-DefaultProfile</span></span>
<span data-ttu-id="bcc09-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bcc09-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcc09-131">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="bcc09-131">-PasswordResetPolicyName</span></span>
<span data-ttu-id="bcc09-132">Name der Richtlinie für die Kennwortzurücksetzung.</span><span class="sxs-lookup"><span data-stu-id="bcc09-132">Password Reset Policy Name.</span></span> <span data-ttu-id="bcc09-133">Gilt nur für AAD B2C-Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="bcc09-133">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="bcc09-134">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="bcc09-134">This parameter is optional.</span></span>

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

### <span data-ttu-id="bcc09-135">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="bcc09-135">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="bcc09-136">Name der Profilbearbeitungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="bcc09-136">Profile Editing Policy Name.</span></span> <span data-ttu-id="bcc09-137">Gilt nur für AAD B2C-Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="bcc09-137">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="bcc09-138">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="bcc09-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="bcc09-139">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="bcc09-139">-SigninPolicyName</span></span>
<span data-ttu-id="bcc09-140">Name der Anmelderichtlinie.</span><span class="sxs-lookup"><span data-stu-id="bcc09-140">Signin Policy Name.</span></span> <span data-ttu-id="bcc09-141">Gilt nur für AAD B2C-Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="bcc09-141">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="bcc09-142">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="bcc09-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="bcc09-143">-SigninTenant</span><span class="sxs-lookup"><span data-stu-id="bcc09-143">-SigninTenant</span></span>
<span data-ttu-id="bcc09-144">Signin Tenant to override in AAD B2C instead of the `common` Tenant</span><span class="sxs-lookup"><span data-stu-id="bcc09-144">Signin Tenant to override in AAD B2C instead of the `common` Tenant</span></span>

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

### <span data-ttu-id="bcc09-145">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="bcc09-145">-SignupPolicyName</span></span>
<span data-ttu-id="bcc09-146">Name der Anmelderichtlinie.</span><span class="sxs-lookup"><span data-stu-id="bcc09-146">Signup Policy Name.</span></span> <span data-ttu-id="bcc09-147">Gilt nur für AAD B2C-Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="bcc09-147">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="bcc09-148">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="bcc09-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="bcc09-149">-Type</span><span class="sxs-lookup"><span data-stu-id="bcc09-149">-Type</span></span>
<span data-ttu-id="bcc09-150">Id eines Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="bcc09-150">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="bcc09-151">Bei Angabe wird versucht, die Konfiguration des Identitätsanbieters nach dem Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="bcc09-151">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="bcc09-152">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="bcc09-152">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcc09-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bcc09-153">-Confirm</span></span>
<span data-ttu-id="bcc09-154">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bcc09-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcc09-155">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="bcc09-155">-WhatIf</span></span>
<span data-ttu-id="bcc09-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bcc09-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bcc09-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bcc09-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcc09-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcc09-158">CommonParameters</span></span>
<span data-ttu-id="bcc09-159">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcc09-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcc09-160">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bcc09-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcc09-161">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bcc09-161">INPUTS</span></span>

### <span data-ttu-id="bcc09-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bcc09-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bcc09-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="bcc09-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="bcc09-164">System.String</span><span class="sxs-lookup"><span data-stu-id="bcc09-164">System.String</span></span>

### <span data-ttu-id="bcc09-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="bcc09-165">System.String[]</span></span>

## <span data-ttu-id="bcc09-166">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bcc09-166">OUTPUTS</span></span>

### <span data-ttu-id="bcc09-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="bcc09-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="bcc09-168">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bcc09-168">NOTES</span></span>

## <span data-ttu-id="bcc09-169">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bcc09-169">RELATED LINKS</span></span>

[<span data-ttu-id="bcc09-170">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="bcc09-170">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="bcc09-171">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="bcc09-171">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="bcc09-172">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="bcc09-172">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)
