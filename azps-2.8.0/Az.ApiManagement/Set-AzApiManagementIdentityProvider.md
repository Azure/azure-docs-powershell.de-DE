---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
ms.openlocfilehash: d2d689c9df73f7cd9bb6df6a5153e9afa71cb39d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658143"
---
# <span data-ttu-id="865a5-101">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="865a5-101">Set-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="865a5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="865a5-102">SYNOPSIS</span></span>
<span data-ttu-id="865a5-103">Aktualisiert die Konfiguration eines vorhandenen Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="865a5-103">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="865a5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="865a5-104">SYNTAX</span></span>

### <span data-ttu-id="865a5-105">Expanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="865a5-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="865a5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="865a5-106">ByInputObject</span></span>
```
Set-AzApiManagementIdentityProvider -InputObject <PsApiManagementIdentityProvider> [-ClientId <String>]
 [-ClientSecret <String>] [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>]
 [-SigninPolicyName <String>] [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="865a5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="865a5-107">DESCRIPTION</span></span>
<span data-ttu-id="865a5-108">Aktualisiert die Konfiguration eines vorhandenen Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="865a5-108">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="865a5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="865a5-109">EXAMPLES</span></span>

### <span data-ttu-id="865a5-110">Beispiel 1: Aktualisieren des Facebook-Identitätsanbieters</span><span class="sxs-lookup"><span data-stu-id="865a5-110">Example 1 : Update the facebook Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="865a5-111">Das Cmdlet aktualisiert den Client Schlüssel des Facebook-Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="865a5-111">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="865a5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="865a5-112">PARAMETERS</span></span>

### <span data-ttu-id="865a5-113">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="865a5-113">-AllowedTenants</span></span>
<span data-ttu-id="865a5-114">Liste der zulässigen Azure Active Directory-Mandanten.</span><span class="sxs-lookup"><span data-stu-id="865a5-114">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="865a5-115">-Authority</span><span class="sxs-lookup"><span data-stu-id="865a5-115">-Authority</span></span>
<span data-ttu-id="865a5-116">OpenID Connect Discovery-Endpunkt-Hostname für Aad oder Aad B2C.</span><span class="sxs-lookup"><span data-stu-id="865a5-116">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="865a5-117">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="865a5-117">This parameter is optional.</span></span>

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

### <span data-ttu-id="865a5-118">-ClientID</span><span class="sxs-lookup"><span data-stu-id="865a5-118">-ClientId</span></span>
<span data-ttu-id="865a5-119">Client-ID der Anwendung im externen Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="865a5-119">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="865a5-120">Es ist die APP-ID für Facebook-Anmeldung, Client-ID für Google-Anmeldung, APP-ID für Microsoft.</span><span class="sxs-lookup"><span data-stu-id="865a5-120">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="865a5-121">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="865a5-121">-ClientSecret</span></span>
<span data-ttu-id="865a5-122">Client-Schlüssel der Anwendung im externen Identitätsanbieter, der zur Authentifizierung der Anmeldeanforderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="865a5-122">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="865a5-123">Beispielsweise ist es App Secret für Facebook-Anmeldung, API-Schlüssel für Google-Anmeldung, öffentlicher Schlüssel für Microsoft.</span><span class="sxs-lookup"><span data-stu-id="865a5-123">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="865a5-124">-Context</span><span class="sxs-lookup"><span data-stu-id="865a5-124">-Context</span></span>
<span data-ttu-id="865a5-125">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="865a5-125">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="865a5-126">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="865a5-126">This parameter is required.</span></span>

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

### <span data-ttu-id="865a5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="865a5-127">-DefaultProfile</span></span>
<span data-ttu-id="865a5-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="865a5-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="865a5-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="865a5-129">-InputObject</span></span>
<span data-ttu-id="865a5-130">Instanz von PsApiManagementIdentityProvider.</span><span class="sxs-lookup"><span data-stu-id="865a5-130">Instance of PsApiManagementIdentityProvider.</span></span> <span data-ttu-id="865a5-131">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="865a5-131">This parameter is required.</span></span>

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

### <span data-ttu-id="865a5-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="865a5-132">-PassThru</span></span>
<span data-ttu-id="865a5-133">Gibt an, dass dieses Cmdlet die  **PsApiManagementIdentityProvider** zurückgibt, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="865a5-133">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="865a5-134">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="865a5-134">-PasswordResetPolicyName</span></span>
<span data-ttu-id="865a5-135">Richtlinien Name für Kennwortzurücksetzung</span><span class="sxs-lookup"><span data-stu-id="865a5-135">Password Reset Policy Name.</span></span> <span data-ttu-id="865a5-136">Gilt nur für Aad B2C-Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="865a5-136">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="865a5-137">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="865a5-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="865a5-138">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="865a5-138">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="865a5-139">Name der Profil Bearbeitungs Richtlinie</span><span class="sxs-lookup"><span data-stu-id="865a5-139">Profile Editing Policy Name.</span></span> <span data-ttu-id="865a5-140">Gilt nur für Aad B2C-Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="865a5-140">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="865a5-141">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="865a5-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="865a5-142">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="865a5-142">-SigninPolicyName</span></span>
<span data-ttu-id="865a5-143">Name der SignIn-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="865a5-143">Signin Policy Name.</span></span> <span data-ttu-id="865a5-144">Gilt nur für Aad B2C-Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="865a5-144">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="865a5-145">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="865a5-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="865a5-146">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="865a5-146">-SignupPolicyName</span></span>
<span data-ttu-id="865a5-147">Name der Anmelderichtlinie</span><span class="sxs-lookup"><span data-stu-id="865a5-147">Signup Policy Name.</span></span> <span data-ttu-id="865a5-148">Gilt nur für Aad B2C-Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="865a5-148">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="865a5-149">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="865a5-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="865a5-150">-Typ</span><span class="sxs-lookup"><span data-stu-id="865a5-150">-Type</span></span>
<span data-ttu-id="865a5-151">Bezeichner eines vorhandenen Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="865a5-151">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="865a5-152">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="865a5-152">This parameter is required.</span></span>

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

### <span data-ttu-id="865a5-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="865a5-153">-Confirm</span></span>
<span data-ttu-id="865a5-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="865a5-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="865a5-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="865a5-155">-WhatIf</span></span>
<span data-ttu-id="865a5-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="865a5-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="865a5-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="865a5-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="865a5-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="865a5-158">CommonParameters</span></span>
<span data-ttu-id="865a5-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="865a5-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="865a5-160">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="865a5-160">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="865a5-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="865a5-161">INPUTS</span></span>

### <span data-ttu-id="865a5-162">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="865a5-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="865a5-163">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="865a5-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="865a5-164">System. String</span><span class="sxs-lookup"><span data-stu-id="865a5-164">System.String</span></span>

### <span data-ttu-id="865a5-165">System. String []</span><span class="sxs-lookup"><span data-stu-id="865a5-165">System.String[]</span></span>

### <span data-ttu-id="865a5-166">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="865a5-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="865a5-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="865a5-167">OUTPUTS</span></span>

### <span data-ttu-id="865a5-168">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="865a5-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="865a5-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="865a5-169">NOTES</span></span>

## <span data-ttu-id="865a5-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="865a5-170">RELATED LINKS</span></span>

[<span data-ttu-id="865a5-171">Neu – AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="865a5-171">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="865a5-172">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="865a5-172">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="865a5-173">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="865a5-173">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)
