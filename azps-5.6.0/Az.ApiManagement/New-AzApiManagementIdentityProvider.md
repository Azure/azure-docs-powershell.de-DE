---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 31a635c5965d40cf12e77d556e987c08dfb7175a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939779"
---
# <span data-ttu-id="7ff22-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="7ff22-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="7ff22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ff22-102">SYNOPSIS</span></span>
<span data-ttu-id="7ff22-103">Erstellt eine neue Konfiguration des Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="7ff22-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="7ff22-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ff22-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-SigninTenant <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ff22-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ff22-105">DESCRIPTION</span></span>
<span data-ttu-id="7ff22-106">Erstellt eine neue Konfiguration des Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="7ff22-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="7ff22-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7ff22-107">EXAMPLES</span></span>

### <span data-ttu-id="7ff22-108">Beispiel 1: Konfigurieren von Facebook als Identitätsanbieter für Entwicklerportalanmeldungen</span><span class="sxs-lookup"><span data-stu-id="7ff22-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="7ff22-109">Mit diesem Befehl wird die Facebook-Identität als akzeptierter Identitätsanbieter im Entwicklerportal des ApiManagement-Diensts konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="7ff22-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="7ff22-110">Dies nimmt als Eingabe die ClientId und ClientSecret der Facebook-App an.</span><span class="sxs-lookup"><span data-stu-id="7ff22-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

### <span data-ttu-id="7ff22-111">Beispiel 2: Konfigurieren von adB2C als Identitätsanbieter für Entwicklerportalanmeldungen</span><span class="sxs-lookup"><span data-stu-id="7ff22-111">Example 2: Configures adB2C as an identity Provider for Developer Portal Logins</span></span>
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

<span data-ttu-id="7ff22-112">Mit diesem Befehl wird die Facebook-Identität als akzeptierter Identitätsanbieter im Entwicklerportal des ApiManagement-Diensts konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="7ff22-112">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="7ff22-113">Dies nimmt als Eingabe die ClientId und ClientSecret der Facebook-App an.</span><span class="sxs-lookup"><span data-stu-id="7ff22-113">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="7ff22-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7ff22-114">PARAMETERS</span></span>

### <span data-ttu-id="7ff22-115">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="7ff22-115">-AllowedTenants</span></span>
<span data-ttu-id="7ff22-116">Liste der zulässigen Azure Active Directory-Mandanten</span><span class="sxs-lookup"><span data-stu-id="7ff22-116">List of allowed Azure Active Directory Tenants</span></span>

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

### <span data-ttu-id="7ff22-117">-Autorität</span><span class="sxs-lookup"><span data-stu-id="7ff22-117">-Authority</span></span>
<span data-ttu-id="7ff22-118">OpenID Connect Discovery-Endpunkt hostname für AAD oder AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="7ff22-118">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="7ff22-119">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="7ff22-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="7ff22-120">-ClientId</span><span class="sxs-lookup"><span data-stu-id="7ff22-120">-ClientId</span></span>
<span data-ttu-id="7ff22-121">Client-ID der Anwendung im externen Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="7ff22-121">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="7ff22-122">Dies sind App-ID für Facebook-Anmeldung, Client-ID für Google-Anmeldung, App-ID für Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7ff22-122">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="7ff22-123">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="7ff22-123">-ClientSecret</span></span>
<span data-ttu-id="7ff22-124">Client secret of the Application in external Identity Provider, used to authenticate login request.</span><span class="sxs-lookup"><span data-stu-id="7ff22-124">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="7ff22-125">So handelt es sich z. B. um "App Secret for Facebook login", "API Key for Google login", "Public Key" für Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7ff22-125">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="7ff22-126">-Context</span><span class="sxs-lookup"><span data-stu-id="7ff22-126">-Context</span></span>
<span data-ttu-id="7ff22-127">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7ff22-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7ff22-128">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7ff22-128">This parameter is required.</span></span>

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

### <span data-ttu-id="7ff22-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ff22-129">-DefaultProfile</span></span>
<span data-ttu-id="7ff22-130">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ff22-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ff22-131">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="7ff22-131">-PasswordResetPolicyName</span></span>
<span data-ttu-id="7ff22-132">Name der Kennwortzurücksetzungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="7ff22-132">Password Reset Policy Name.</span></span> <span data-ttu-id="7ff22-133">Gilt nur für AAD B2C-Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="7ff22-133">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="7ff22-134">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="7ff22-134">This parameter is optional.</span></span>

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

### <span data-ttu-id="7ff22-135">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="7ff22-135">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="7ff22-136">Name der Profilbearbeitungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="7ff22-136">Profile Editing Policy Name.</span></span> <span data-ttu-id="7ff22-137">Gilt nur für AAD B2C-Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="7ff22-137">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="7ff22-138">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="7ff22-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="7ff22-139">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="7ff22-139">-SigninPolicyName</span></span>
<span data-ttu-id="7ff22-140">Name der Anmelderichtlinie.</span><span class="sxs-lookup"><span data-stu-id="7ff22-140">Signin Policy Name.</span></span> <span data-ttu-id="7ff22-141">Gilt nur für AAD B2C-Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="7ff22-141">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="7ff22-142">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="7ff22-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="7ff22-143">-SigninTenant</span><span class="sxs-lookup"><span data-stu-id="7ff22-143">-SigninTenant</span></span>
<span data-ttu-id="7ff22-144">Signin Tenant to override in AAD B2C statt `common` tenant</span><span class="sxs-lookup"><span data-stu-id="7ff22-144">Signin Tenant to override in AAD B2C instead of the `common` Tenant</span></span>

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

### <span data-ttu-id="7ff22-145">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="7ff22-145">-SignupPolicyName</span></span>
<span data-ttu-id="7ff22-146">Name der Anmelderichtlinie.</span><span class="sxs-lookup"><span data-stu-id="7ff22-146">Signup Policy Name.</span></span> <span data-ttu-id="7ff22-147">Gilt nur für AAD B2C-Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="7ff22-147">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="7ff22-148">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="7ff22-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="7ff22-149">-Type</span><span class="sxs-lookup"><span data-stu-id="7ff22-149">-Type</span></span>
<span data-ttu-id="7ff22-150">Bezeichner eines Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="7ff22-150">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="7ff22-151">Wenn angegeben, wird versucht, die Konfiguration des Identitätsanbieters durch den Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="7ff22-151">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="7ff22-152">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="7ff22-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="7ff22-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7ff22-153">-Confirm</span></span>
<span data-ttu-id="7ff22-154">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7ff22-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ff22-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ff22-155">-WhatIf</span></span>
<span data-ttu-id="7ff22-156">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7ff22-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ff22-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7ff22-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ff22-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ff22-158">CommonParameters</span></span>
<span data-ttu-id="7ff22-159">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ff22-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ff22-160">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ff22-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ff22-161">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7ff22-161">INPUTS</span></span>

### <span data-ttu-id="7ff22-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7ff22-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7ff22-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="7ff22-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="7ff22-164">System.String</span><span class="sxs-lookup"><span data-stu-id="7ff22-164">System.String</span></span>

### <span data-ttu-id="7ff22-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="7ff22-165">System.String[]</span></span>

## <span data-ttu-id="7ff22-166">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7ff22-166">OUTPUTS</span></span>

### <span data-ttu-id="7ff22-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="7ff22-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="7ff22-168">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7ff22-168">NOTES</span></span>

## <span data-ttu-id="7ff22-169">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7ff22-169">RELATED LINKS</span></span>

[<span data-ttu-id="7ff22-170">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="7ff22-170">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="7ff22-171">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="7ff22-171">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="7ff22-172">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="7ff22-172">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)
