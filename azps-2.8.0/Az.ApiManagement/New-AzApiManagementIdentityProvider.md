---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: fc033eb1989838d8ed8e20d568f92ef20f8275e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658247"
---
# <span data-ttu-id="28db4-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="28db4-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="28db4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="28db4-102">SYNOPSIS</span></span>
<span data-ttu-id="28db4-103">Erstellt eine neue Identität Anbieterkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="28db4-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="28db4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="28db4-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28db4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28db4-105">DESCRIPTION</span></span>
<span data-ttu-id="28db4-106">Erstellt eine neue Identität Anbieterkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="28db4-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="28db4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="28db4-107">EXAMPLES</span></span>

### <span data-ttu-id="28db4-108">Beispiel 1: konfiguriert Facebook als Identitätsanbieter für Entwickler Portal-Anmeldungen</span><span class="sxs-lookup"><span data-stu-id="28db4-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="28db4-109">Dieser Befehl konfiguriert die Facebook-Identität als akzeptierter Identitätsanbieter im Entwickler Portal des ApiManagement-Diensts.</span><span class="sxs-lookup"><span data-stu-id="28db4-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="28db4-110">Dies erfordert die Eingabe der ClientID und ClientSecret der Facebook-App.</span><span class="sxs-lookup"><span data-stu-id="28db4-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

### <span data-ttu-id="28db4-111">Beispiel 2: Konfigurieren von adB2C als Identitätsanbieter für Entwickler Portal-Anmeldungen</span><span class="sxs-lookup"><span data-stu-id="28db4-111">Example 2: Configures adB2C as an identity Provider for Developer Portal Logins</span></span>
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

<span data-ttu-id="28db4-112">Dieser Befehl konfiguriert die Facebook-Identität als akzeptierter Identitätsanbieter im Entwickler Portal des ApiManagement-Diensts.</span><span class="sxs-lookup"><span data-stu-id="28db4-112">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="28db4-113">Dies erfordert die Eingabe der ClientID und ClientSecret der Facebook-App.</span><span class="sxs-lookup"><span data-stu-id="28db4-113">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="28db4-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="28db4-114">PARAMETERS</span></span>

### <span data-ttu-id="28db4-115">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="28db4-115">-AllowedTenants</span></span>
<span data-ttu-id="28db4-116">Liste der zulässigen Azure Active Directory-Mandanten</span><span class="sxs-lookup"><span data-stu-id="28db4-116">List of allowed Azure Active Directory Tenants</span></span>

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

### <span data-ttu-id="28db4-117">-Authority</span><span class="sxs-lookup"><span data-stu-id="28db4-117">-Authority</span></span>
<span data-ttu-id="28db4-118">OpenID Connect Discovery-Endpunkt-Hostname für Aad oder Aad B2C.</span><span class="sxs-lookup"><span data-stu-id="28db4-118">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="28db4-119">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="28db4-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="28db4-120">-ClientID</span><span class="sxs-lookup"><span data-stu-id="28db4-120">-ClientId</span></span>
<span data-ttu-id="28db4-121">Client-ID der Anwendung im externen Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="28db4-121">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="28db4-122">Es ist die APP-ID für Facebook-Anmeldung, Client-ID für Google-Anmeldung, APP-ID für Microsoft.</span><span class="sxs-lookup"><span data-stu-id="28db4-122">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="28db4-123">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="28db4-123">-ClientSecret</span></span>
<span data-ttu-id="28db4-124">Client-Schlüssel der Anwendung im externen Identitätsanbieter, der zur Authentifizierung der Anmeldeanforderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="28db4-124">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="28db4-125">Beispielsweise ist es App Secret für Facebook-Anmeldung, API-Schlüssel für Google-Anmeldung, öffentlicher Schlüssel für Microsoft.</span><span class="sxs-lookup"><span data-stu-id="28db4-125">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="28db4-126">-Context</span><span class="sxs-lookup"><span data-stu-id="28db4-126">-Context</span></span>
<span data-ttu-id="28db4-127">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="28db4-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="28db4-128">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="28db4-128">This parameter is required.</span></span>

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

### <span data-ttu-id="28db4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28db4-129">-DefaultProfile</span></span>
<span data-ttu-id="28db4-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="28db4-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28db4-131">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="28db4-131">-PasswordResetPolicyName</span></span>
<span data-ttu-id="28db4-132">Richtlinien Name für Kennwortzurücksetzung</span><span class="sxs-lookup"><span data-stu-id="28db4-132">Password Reset Policy Name.</span></span> <span data-ttu-id="28db4-133">Gilt nur für Aad B2C-Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="28db4-133">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="28db4-134">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="28db4-134">This parameter is optional.</span></span>

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

### <span data-ttu-id="28db4-135">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="28db4-135">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="28db4-136">Name der Profil Bearbeitungs Richtlinie</span><span class="sxs-lookup"><span data-stu-id="28db4-136">Profile Editing Policy Name.</span></span> <span data-ttu-id="28db4-137">Gilt nur für Aad B2C-Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="28db4-137">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="28db4-138">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="28db4-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="28db4-139">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="28db4-139">-SigninPolicyName</span></span>
<span data-ttu-id="28db4-140">Name der SignIn-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="28db4-140">Signin Policy Name.</span></span> <span data-ttu-id="28db4-141">Gilt nur für Aad B2C-Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="28db4-141">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="28db4-142">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="28db4-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="28db4-143">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="28db4-143">-SignupPolicyName</span></span>
<span data-ttu-id="28db4-144">Name der Anmelderichtlinie</span><span class="sxs-lookup"><span data-stu-id="28db4-144">Signup Policy Name.</span></span> <span data-ttu-id="28db4-145">Gilt nur für Aad B2C-Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="28db4-145">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="28db4-146">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="28db4-146">This parameter is optional.</span></span>

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

### <span data-ttu-id="28db4-147">-Typ</span><span class="sxs-lookup"><span data-stu-id="28db4-147">-Type</span></span>
<span data-ttu-id="28db4-148">Bezeichner eines Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="28db4-148">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="28db4-149">Wenn angegeben, wird versucht, die Konfiguration des Identitätsanbieters anhand des Bezeichners zu finden.</span><span class="sxs-lookup"><span data-stu-id="28db4-149">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="28db4-150">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="28db4-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="28db4-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="28db4-151">-Confirm</span></span>
<span data-ttu-id="28db4-152">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="28db4-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28db4-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28db4-153">-WhatIf</span></span>
<span data-ttu-id="28db4-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="28db4-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28db4-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="28db4-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28db4-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28db4-156">CommonParameters</span></span>
<span data-ttu-id="28db4-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28db4-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28db4-158">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28db4-158">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28db4-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="28db4-159">INPUTS</span></span>

### <span data-ttu-id="28db4-160">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="28db4-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="28db4-161">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="28db4-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="28db4-162">System. String</span><span class="sxs-lookup"><span data-stu-id="28db4-162">System.String</span></span>

### <span data-ttu-id="28db4-163">System. String []</span><span class="sxs-lookup"><span data-stu-id="28db4-163">System.String[]</span></span>

## <span data-ttu-id="28db4-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="28db4-164">OUTPUTS</span></span>

### <span data-ttu-id="28db4-165">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="28db4-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="28db4-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="28db4-166">NOTES</span></span>

## <span data-ttu-id="28db4-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="28db4-167">RELATED LINKS</span></span>

[<span data-ttu-id="28db4-168">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="28db4-168">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="28db4-169">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="28db4-169">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="28db4-170">Satz-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="28db4-170">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)
