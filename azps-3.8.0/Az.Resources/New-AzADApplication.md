---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
ms.openlocfilehash: a60e2b873803c8ad3acfdc08c645cf419cf8689f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004666"
---
# <span data-ttu-id="17120-101">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="17120-101">New-AzADApplication</span></span>

## <span data-ttu-id="17120-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="17120-102">SYNOPSIS</span></span>
<span data-ttu-id="17120-103">Erstellt eine neue Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="17120-103">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="17120-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="17120-104">SYNTAX</span></span>

### <span data-ttu-id="17120-105">ApplicationWithoutCredentialParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="17120-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17120-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="17120-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17120-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="17120-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17120-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="17120-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17120-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="17120-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17120-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17120-110">DESCRIPTION</span></span>
<span data-ttu-id="17120-111">Erstellt eine neue Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="17120-111">Creates a new azure active directory application.</span></span> <span data-ttu-id="17120-112">Im folgenden finden Sie die erforderlichen Berechtigungen zum Erstellen einer Anwendung:</span><span class="sxs-lookup"><span data-stu-id="17120-112">Below are the permissions needed to create an application:</span></span>

- <span data-ttu-id="17120-113">Azure Active Directory-Diagramm</span><span class="sxs-lookup"><span data-stu-id="17120-113">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="17120-114">Application. ReadWrite. OwnedBy</span><span class="sxs-lookup"><span data-stu-id="17120-114">Application.ReadWrite.OwnedBy</span></span>
- <span data-ttu-id="17120-115">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="17120-115">Microsoft Graph</span></span>
  - <span data-ttu-id="17120-116">Directory. AccessAsUser. all</span><span class="sxs-lookup"><span data-stu-id="17120-116">Directory.AccessAsUser.All</span></span>
  - <span data-ttu-id="17120-117">Directory. ReadWrite. all</span><span class="sxs-lookup"><span data-stu-id="17120-117">Directory.ReadWrite.All</span></span>

## <span data-ttu-id="17120-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="17120-118">EXAMPLES</span></span>

### <span data-ttu-id="17120-119">Beispiel 1: Erstellen einer neuen Aad-Anwendung</span><span class="sxs-lookup"><span data-stu-id="17120-119">Example 1 - Create new AAD application.</span></span>

```
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="17120-120">Erstellt eine neue Azure Active Directory-Anwendung ohne Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="17120-120">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="17120-121">Beispiel 2: Erstellen einer neuen Aad-Anwendung mit einem Kennwort</span><span class="sxs-lookup"><span data-stu-id="17120-121">Example 2 - Create new AAD application with password.</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="17120-122">Erstellt eine neue Azure Active Directory-Anwendung und ordnet dem Kennwort Anmeldeinformationen zu.</span><span class="sxs-lookup"><span data-stu-id="17120-122">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="17120-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="17120-123">PARAMETERS</span></span>

### <span data-ttu-id="17120-124">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="17120-124">-AvailableToOtherTenants</span></span>
<span data-ttu-id="17120-125">Der Wert, der angibt, ob es sich bei der Anwendung um einen einzelnen Mandanten oder um einen Mandanten handelt.</span><span class="sxs-lookup"><span data-stu-id="17120-125">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

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

### <span data-ttu-id="17120-126">-Certvalue</span><span class="sxs-lookup"><span data-stu-id="17120-126">-CertValue</span></span>
<span data-ttu-id="17120-127">Der Wert des Anmeldeinformationstyps "asymmetrisch".</span><span class="sxs-lookup"><span data-stu-id="17120-127">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="17120-128">Es stellt das Basis 64-codierte Zertifikat dar.</span><span class="sxs-lookup"><span data-stu-id="17120-128">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="17120-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17120-129">-DefaultProfile</span></span>
<span data-ttu-id="17120-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="17120-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17120-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="17120-131">-DisplayName</span></span>
<span data-ttu-id="17120-132">Der Anzeigename der neuen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="17120-132">Display name of the new application.</span></span>

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

### <span data-ttu-id="17120-133">-Enddate</span><span class="sxs-lookup"><span data-stu-id="17120-133">-EndDate</span></span>
<span data-ttu-id="17120-134">Das effektive Enddatum der Anmelde Informationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="17120-134">The effective end date of the credential usage.</span></span>
<span data-ttu-id="17120-135">Der Standardwert für Enddatum beträgt ein Jahr ab heute.</span><span class="sxs-lookup"><span data-stu-id="17120-135">The default end date value is one year from today.</span></span> <span data-ttu-id="17120-136">Bei einer "asymmetrischen" Art von Anmeldeinformationen muss dies auf ein oder vor dem Datum festgesetzt werden, an dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="17120-136">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="17120-137">-Startseite</span><span class="sxs-lookup"><span data-stu-id="17120-137">-HomePage</span></span>
<span data-ttu-id="17120-138">Die URL zur Startseite der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="17120-138">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="17120-139">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="17120-139">-IdentifierUris</span></span>
<span data-ttu-id="17120-140">Die URIs, die die Anwendung identifizieren.</span><span class="sxs-lookup"><span data-stu-id="17120-140">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="17120-141">-Keycredentials</span><span class="sxs-lookup"><span data-stu-id="17120-141">-KeyCredentials</span></span>
<span data-ttu-id="17120-142">Die Liste der Zertifikatanmeldeinformationen, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="17120-142">The list of certificate credentials associated with the application.</span></span>

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

### <span data-ttu-id="17120-143">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="17120-143">-Password</span></span>
<span data-ttu-id="17120-144">Das Kennwort, das der Anwendung zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="17120-144">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="17120-145">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="17120-145">-PasswordCredentials</span></span>
<span data-ttu-id="17120-146">Die Liste der Kennwortanmeldeinformationen, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="17120-146">The list of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="17120-147">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="17120-147">-ReplyUrls</span></span>
<span data-ttu-id="17120-148">Die URL der Anwendungsantwort.</span><span class="sxs-lookup"><span data-stu-id="17120-148">The application reply urls.</span></span>

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

### <span data-ttu-id="17120-149">-StartDate</span><span class="sxs-lookup"><span data-stu-id="17120-149">-StartDate</span></span>
<span data-ttu-id="17120-150">Der effektive Anfangstermin der Anmelde Informationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="17120-150">The effective start date of the credential usage.</span></span>
<span data-ttu-id="17120-151">Der Standardwert für das Anfangsdatum ist heute.</span><span class="sxs-lookup"><span data-stu-id="17120-151">The default start date value is today.</span></span> <span data-ttu-id="17120-152">Bei einer "asymmetrischen" Art von Anmeldeinformationen muss dies auf ein oder nach dem Datum festgesetzt werden, ab dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="17120-152">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="17120-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="17120-153">-Confirm</span></span>
<span data-ttu-id="17120-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="17120-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17120-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17120-155">-WhatIf</span></span>
<span data-ttu-id="17120-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="17120-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17120-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="17120-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17120-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17120-158">CommonParameters</span></span>
<span data-ttu-id="17120-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17120-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17120-160">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17120-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17120-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="17120-161">INPUTS</span></span>

### <span data-ttu-id="17120-162">System. String</span><span class="sxs-lookup"><span data-stu-id="17120-162">System.String</span></span>

### <span data-ttu-id="17120-163">System. String []</span><span class="sxs-lookup"><span data-stu-id="17120-163">System.String[]</span></span>

### <span data-ttu-id="17120-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="17120-164">System.Boolean</span></span>

### <span data-ttu-id="17120-165">Microsoft. Azure. Commands. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="17120-165">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="17120-166">Microsoft. Azure. Commands. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="17120-166">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="17120-167">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="17120-167">System.Security.SecureString</span></span>

### <span data-ttu-id="17120-168">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="17120-168">System.DateTime</span></span>

## <span data-ttu-id="17120-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="17120-169">OUTPUTS</span></span>

### <span data-ttu-id="17120-170">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="17120-170">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="17120-171">Notizen</span><span class="sxs-lookup"><span data-stu-id="17120-171">NOTES</span></span>
<span data-ttu-id="17120-172">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="17120-172">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="17120-173">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="17120-173">RELATED LINKS</span></span>

[<span data-ttu-id="17120-174">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="17120-174">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="17120-175">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="17120-175">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="17120-176">Neu – AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="17120-176">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="17120-177">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="17120-177">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="17120-178">Neu – AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="17120-178">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="17120-179">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="17120-179">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

