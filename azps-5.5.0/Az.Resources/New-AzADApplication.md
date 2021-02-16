---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
ms.openlocfilehash: 7ab7c679bc623a9eaa0f99bcdba1ab8281bd7d8f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169116"
---
# <span data-ttu-id="2e5bc-101">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="2e5bc-101">New-AzADApplication</span></span>

## <span data-ttu-id="2e5bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e5bc-102">SYNOPSIS</span></span>
<span data-ttu-id="2e5bc-103">Erstellt eine neue Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-103">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="2e5bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e5bc-104">SYNTAX</span></span>

### <span data-ttu-id="2e5bc-105">ApplicationWithoutCredentialParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2e5bc-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e5bc-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e5bc-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e5bc-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e5bc-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e5bc-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e5bc-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e5bc-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e5bc-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e5bc-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2e5bc-110">DESCRIPTION</span></span>
<span data-ttu-id="2e5bc-111">Erstellt eine neue Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-111">Creates a new azure active directory application.</span></span> <span data-ttu-id="2e5bc-112">Im Folgenden finden Sie die berechtigungen, die zum Erstellen einer Anwendung erforderlich sind:</span><span class="sxs-lookup"><span data-stu-id="2e5bc-112">Below are the permissions needed to create an application:</span></span>

- <span data-ttu-id="2e5bc-113">Azure Active Directory Graph</span><span class="sxs-lookup"><span data-stu-id="2e5bc-113">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="2e5bc-114">Application.ReadWrite.OwnedBy</span><span class="sxs-lookup"><span data-stu-id="2e5bc-114">Application.ReadWrite.OwnedBy</span></span>
- <span data-ttu-id="2e5bc-115">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="2e5bc-115">Microsoft Graph</span></span>
  - <span data-ttu-id="2e5bc-116">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="2e5bc-116">Directory.AccessAsUser.All</span></span>
  - <span data-ttu-id="2e5bc-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2e5bc-117">Directory.ReadWrite.All</span></span>

## <span data-ttu-id="2e5bc-118">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2e5bc-118">EXAMPLES</span></span>

### <span data-ttu-id="2e5bc-119">Beispiel 1: Erstellen einer neuen AAD-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-119">Example 1: Create new AAD application.</span></span>

```powershell
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="2e5bc-120">Erstellt eine neue Azure Active Directory-Anwendung ohne Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-120">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="2e5bc-121">Beispiel 2: Erstellen einer neuen Anwendung AAD mit Kennwort.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-121">Example 2: Create new AAD application with password.</span></span>

```powershell
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="2e5bc-122">Erstellt eine neue Azure Active Directory-Anwendung und ordnet ihr Kennwortanmeldeinformationen zu.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-122">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="2e5bc-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e5bc-123">PARAMETERS</span></span>

### <span data-ttu-id="2e5bc-124">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="2e5bc-124">-AvailableToOtherTenants</span></span>
<span data-ttu-id="2e5bc-125">Der Wert, der an gibt, ob es sich bei der Anwendung um einen einzigen Mandanten oder mehrere Mandanten handelt.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-125">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e5bc-126">-CertValue</span><span class="sxs-lookup"><span data-stu-id="2e5bc-126">-CertValue</span></span>
<span data-ttu-id="2e5bc-127">Der Wert des "asymmetrischen" Anmeldeinformationstyps.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-127">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="2e5bc-128">Es stellt das 64-codierte Basiszertifikat dar.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-128">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e5bc-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e5bc-129">-DefaultProfile</span></span>
<span data-ttu-id="2e5bc-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="2e5bc-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e5bc-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2e5bc-131">-DisplayName</span></span>
<span data-ttu-id="2e5bc-132">Anzeigename der neuen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-132">Display name of the new application.</span></span>

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

### <span data-ttu-id="2e5bc-133">-EndDate</span><span class="sxs-lookup"><span data-stu-id="2e5bc-133">-EndDate</span></span>
<span data-ttu-id="2e5bc-134">Das Effektive Enddatum der Verwendung der Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-134">The effective end date of the credential usage.</span></span>
<span data-ttu-id="2e5bc-135">Der Standardmäßige Enddatumswert liegt ein Jahr nach heute.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-135">The default end date value is one year from today.</span></span> <span data-ttu-id="2e5bc-136">Bei Anmeldeinformationen vom Typ "asymmetrischer Art" muss dies auf das Datum oder vor dem Datum festgelegt werden, an dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-136">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e5bc-137">-HomePage</span><span class="sxs-lookup"><span data-stu-id="2e5bc-137">-HomePage</span></span>
<span data-ttu-id="2e5bc-138">Die URL der Anwendungshomepage.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-138">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="2e5bc-139">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="2e5bc-139">-IdentifierUris</span></span>
<span data-ttu-id="2e5bc-140">Die URIs, die die Anwendung identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-140">The URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e5bc-141">-KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="2e5bc-141">-KeyCredentials</span></span>
<span data-ttu-id="2e5bc-142">Die Liste der Der Anwendung zugeordneten Zertifikatanmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-142">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e5bc-143">-Password</span><span class="sxs-lookup"><span data-stu-id="2e5bc-143">-Password</span></span>
<span data-ttu-id="2e5bc-144">Das Kennwort, das der Anwendung zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-144">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e5bc-145">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="2e5bc-145">-PasswordCredentials</span></span>
<span data-ttu-id="2e5bc-146">Die Liste der Kennwortanmeldeinformationen, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-146">The list of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e5bc-147">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="2e5bc-147">-ReplyUrls</span></span>
<span data-ttu-id="2e5bc-148">Die Antwort-URLs der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-148">The application reply urls.</span></span>

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

### <span data-ttu-id="2e5bc-149">-StartDate</span><span class="sxs-lookup"><span data-stu-id="2e5bc-149">-StartDate</span></span>
<span data-ttu-id="2e5bc-150">Das Effektive Startdatum der Verwendung der Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-150">The effective start date of the credential usage.</span></span>
<span data-ttu-id="2e5bc-151">Der Standardwert für das Startdatum ist "Heute".</span><span class="sxs-lookup"><span data-stu-id="2e5bc-151">The default start date value is today.</span></span> <span data-ttu-id="2e5bc-152">Bei Anmeldeinformationen vom Typ "asymmetrischer Art" muss dies auf das Datum oder nach dem Datum festgelegt werden, ab dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-152">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e5bc-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e5bc-153">-Confirm</span></span>
<span data-ttu-id="2e5bc-154">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e5bc-155">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2e5bc-155">-WhatIf</span></span>
<span data-ttu-id="2e5bc-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e5bc-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e5bc-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e5bc-158">CommonParameters</span></span>
<span data-ttu-id="2e5bc-159">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e5bc-160">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e5bc-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e5bc-161">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2e5bc-161">INPUTS</span></span>

### <span data-ttu-id="2e5bc-162">System.String</span><span class="sxs-lookup"><span data-stu-id="2e5bc-162">System.String</span></span>

### <span data-ttu-id="2e5bc-163">System.String[]</span><span class="sxs-lookup"><span data-stu-id="2e5bc-163">System.String[]</span></span>

### <span data-ttu-id="2e5bc-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2e5bc-164">System.Boolean</span></span>

### <span data-ttu-id="2e5bc-165">Microsoft.Azure.Commands.ActiveDirectory.ODERDPasswordCredential[]</span><span class="sxs-lookup"><span data-stu-id="2e5bc-165">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="2e5bc-166">Microsoft.Azure.Commands.ActiveDirectory.WERDENDKeyCredential[]</span><span class="sxs-lookup"><span data-stu-id="2e5bc-166">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="2e5bc-167">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="2e5bc-167">System.Security.SecureString</span></span>

### <span data-ttu-id="2e5bc-168">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="2e5bc-168">System.DateTime</span></span>

## <span data-ttu-id="2e5bc-169">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2e5bc-169">OUTPUTS</span></span>

### <span data-ttu-id="2e5bc-170">Microsoft.Azure.Commands.ActiveDirectory.WERDENDApplication</span><span class="sxs-lookup"><span data-stu-id="2e5bc-170">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="2e5bc-171">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2e5bc-171">NOTES</span></span>
<span data-ttu-id="2e5bc-172">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="2e5bc-172">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="2e5bc-173">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2e5bc-173">RELATED LINKS</span></span>

[<span data-ttu-id="2e5bc-174">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="2e5bc-174">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="2e5bc-175">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="2e5bc-175">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="2e5bc-176">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2e5bc-176">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="2e5bc-177">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="2e5bc-177">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="2e5bc-178">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="2e5bc-178">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="2e5bc-179">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="2e5bc-179">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

