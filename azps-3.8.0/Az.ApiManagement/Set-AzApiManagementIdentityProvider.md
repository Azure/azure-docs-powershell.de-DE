---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
ms.openlocfilehash: a110e950bff46bba7d3c7b5033c01b95ac2397f1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004061"
---
# <span data-ttu-id="31aec-101">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="31aec-101">Set-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="31aec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="31aec-102">SYNOPSIS</span></span>
<span data-ttu-id="31aec-103">Aktualisiert die Konfiguration eines vorhandenen Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="31aec-103">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="31aec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="31aec-104">SYNTAX</span></span>

### <span data-ttu-id="31aec-105">Expanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="31aec-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-SignInTenant <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31aec-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="31aec-106">ByInputObject</span></span>
```
Set-AzApiManagementIdentityProvider -InputObject <PsApiManagementIdentityProvider> [-ClientId <String>]
 [-ClientSecret <String>] [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>]
 [-SigninPolicyName <String>] [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>]
 [-SignInTenant <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31aec-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31aec-107">DESCRIPTION</span></span>
<span data-ttu-id="31aec-108">Aktualisiert die Konfiguration eines vorhandenen Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="31aec-108">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="31aec-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31aec-109">EXAMPLES</span></span>

### <span data-ttu-id="31aec-110">Beispiel 1: Aktualisieren des Facebook-Identitätsanbieters</span><span class="sxs-lookup"><span data-stu-id="31aec-110">Example 1 : Update the facebook Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="31aec-111">Das Cmdlet aktualisiert den Client Schlüssel des Facebook-Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="31aec-111">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="31aec-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="31aec-112">PARAMETERS</span></span>

### <span data-ttu-id="31aec-113">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="31aec-113">-AllowedTenants</span></span>
<span data-ttu-id="31aec-114">Liste der zulässigen Azure Active Directory-Mandanten.</span><span class="sxs-lookup"><span data-stu-id="31aec-114">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="31aec-115">-Authority</span><span class="sxs-lookup"><span data-stu-id="31aec-115">-Authority</span></span>
<span data-ttu-id="31aec-116">OpenID Connect Discovery-Endpunkt-Hostname für Aad oder Aad B2C.</span><span class="sxs-lookup"><span data-stu-id="31aec-116">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="31aec-117">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="31aec-117">This parameter is optional.</span></span>

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

### <span data-ttu-id="31aec-118">-ClientID</span><span class="sxs-lookup"><span data-stu-id="31aec-118">-ClientId</span></span>
<span data-ttu-id="31aec-119">Client-ID der Anwendung im externen Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="31aec-119">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="31aec-120">Es ist die APP-ID für Facebook-Anmeldung, Client-ID für Google-Anmeldung, APP-ID für Microsoft.</span><span class="sxs-lookup"><span data-stu-id="31aec-120">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="31aec-121">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="31aec-121">-ClientSecret</span></span>
<span data-ttu-id="31aec-122">Client-Schlüssel der Anwendung im externen Identitätsanbieter, der zur Authentifizierung der Anmeldeanforderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="31aec-122">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="31aec-123">Beispielsweise ist es App Secret für Facebook-Anmeldung, API-Schlüssel für Google-Anmeldung, öffentlicher Schlüssel für Microsoft.</span><span class="sxs-lookup"><span data-stu-id="31aec-123">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="31aec-124">-Context</span><span class="sxs-lookup"><span data-stu-id="31aec-124">-Context</span></span>
<span data-ttu-id="31aec-125">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="31aec-125">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="31aec-126">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="31aec-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31aec-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31aec-127">-DefaultProfile</span></span>
<span data-ttu-id="31aec-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="31aec-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31aec-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="31aec-129">-InputObject</span></span>
<span data-ttu-id="31aec-130">Instanz von PsApiManagementIdentityProvider.</span><span class="sxs-lookup"><span data-stu-id="31aec-130">Instance of PsApiManagementIdentityProvider.</span></span> <span data-ttu-id="31aec-131">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="31aec-131">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31aec-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31aec-132">-PassThru</span></span>
<span data-ttu-id="31aec-133">Gibt an, dass dieses Cmdlet die  **PsApiManagementIdentityProvider** zurückgibt, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="31aec-133">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="31aec-134">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="31aec-134">-PasswordResetPolicyName</span></span>
<span data-ttu-id="31aec-135">Richtlinien Name für Kennwortzurücksetzung</span><span class="sxs-lookup"><span data-stu-id="31aec-135">Password Reset Policy Name.</span></span> <span data-ttu-id="31aec-136">Gilt nur für Aad B2C-Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="31aec-136">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="31aec-137">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="31aec-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="31aec-138">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="31aec-138">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="31aec-139">Name der Profil Bearbeitungs Richtlinie</span><span class="sxs-lookup"><span data-stu-id="31aec-139">Profile Editing Policy Name.</span></span> <span data-ttu-id="31aec-140">Gilt nur für Aad B2C-Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="31aec-140">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="31aec-141">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="31aec-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="31aec-142">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="31aec-142">-SigninPolicyName</span></span>
<span data-ttu-id="31aec-143">Name der SignIn-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="31aec-143">Signin Policy Name.</span></span> <span data-ttu-id="31aec-144">Gilt nur für Aad B2C-Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="31aec-144">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="31aec-145">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="31aec-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="31aec-146">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="31aec-146">-SignupPolicyName</span></span>
<span data-ttu-id="31aec-147">Name der Anmelderichtlinie</span><span class="sxs-lookup"><span data-stu-id="31aec-147">Signup Policy Name.</span></span> <span data-ttu-id="31aec-148">Gilt nur für Aad B2C-Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="31aec-148">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="31aec-149">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="31aec-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="31aec-150">-Typ</span><span class="sxs-lookup"><span data-stu-id="31aec-150">-Type</span></span>
<span data-ttu-id="31aec-151">Bezeichner eines vorhandenen Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="31aec-151">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="31aec-152">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="31aec-152">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: ExpandedParameter
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31aec-153">-SigninTenant</span><span class="sxs-lookup"><span data-stu-id="31aec-153">-SigninTenant</span></span>
<span data-ttu-id="31aec-154">Anmeldemandant, der in Aad B2C anstelle des Mandanten überschrieben werden soll `common`</span><span class="sxs-lookup"><span data-stu-id="31aec-154">Signin Tenant to override in AAD B2C instead of the `common` Tenant</span></span>

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

### <span data-ttu-id="31aec-155">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="31aec-155">-Confirm</span></span>
<span data-ttu-id="31aec-156">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="31aec-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31aec-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31aec-157">-WhatIf</span></span>
<span data-ttu-id="31aec-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="31aec-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31aec-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="31aec-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31aec-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31aec-160">CommonParameters</span></span>
<span data-ttu-id="31aec-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31aec-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31aec-162">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31aec-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31aec-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="31aec-163">INPUTS</span></span>

### <span data-ttu-id="31aec-164">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="31aec-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="31aec-165">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="31aec-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="31aec-166">System. String</span><span class="sxs-lookup"><span data-stu-id="31aec-166">System.String</span></span>

### <span data-ttu-id="31aec-167">System. String []</span><span class="sxs-lookup"><span data-stu-id="31aec-167">System.String[]</span></span>

### <span data-ttu-id="31aec-168">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="31aec-168">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="31aec-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="31aec-169">OUTPUTS</span></span>

### <span data-ttu-id="31aec-170">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="31aec-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="31aec-171">Notizen</span><span class="sxs-lookup"><span data-stu-id="31aec-171">NOTES</span></span>

## <span data-ttu-id="31aec-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="31aec-172">RELATED LINKS</span></span>

[<span data-ttu-id="31aec-173">Neu – AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="31aec-173">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="31aec-174">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="31aec-174">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="31aec-175">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="31aec-175">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)
