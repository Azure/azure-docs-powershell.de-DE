---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
ms.openlocfilehash: fa861a7be0716ec1da1f2f2a100e7dbbdc97af51
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659613"
---
# <span data-ttu-id="244c6-101">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="244c6-101">New-AzADApplication</span></span>

## <span data-ttu-id="244c6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="244c6-102">SYNOPSIS</span></span>
<span data-ttu-id="244c6-103">Erstellt eine neue Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="244c6-103">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="244c6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="244c6-104">SYNTAX</span></span>

### <span data-ttu-id="244c6-105">ApplicationWithoutCredentialParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="244c6-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="244c6-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="244c6-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="244c6-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="244c6-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="244c6-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="244c6-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="244c6-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="244c6-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="244c6-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="244c6-110">DESCRIPTION</span></span>
<span data-ttu-id="244c6-111">Erstellt eine neue Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="244c6-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="244c6-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="244c6-112">EXAMPLES</span></span>

### <span data-ttu-id="244c6-113">Beispiel 1: Erstellen einer neuen Aad-Anwendung</span><span class="sxs-lookup"><span data-stu-id="244c6-113">Example 1 - Create new AAD application.</span></span>

```
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="244c6-114">Erstellt eine neue Azure Active Directory-Anwendung ohne Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="244c6-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="244c6-115">Beispiel 2: Erstellen einer neuen Aad-Anwendung mit einem Kennwort</span><span class="sxs-lookup"><span data-stu-id="244c6-115">Example 2 - Create new AAD application with password.</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="244c6-116">Erstellt eine neue Azure Active Directory-Anwendung und ordnet dem Kennwort Anmeldeinformationen zu.</span><span class="sxs-lookup"><span data-stu-id="244c6-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="244c6-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="244c6-117">PARAMETERS</span></span>

### <span data-ttu-id="244c6-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="244c6-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="244c6-119">Der Wert, der angibt, ob es sich bei der Anwendung um einen einzelnen Mandanten oder um einen Mandanten handelt.</span><span class="sxs-lookup"><span data-stu-id="244c6-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

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

### <span data-ttu-id="244c6-120">-Certvalue</span><span class="sxs-lookup"><span data-stu-id="244c6-120">-CertValue</span></span>
<span data-ttu-id="244c6-121">Der Wert des Anmeldeinformationstyps "asymmetrisch".</span><span class="sxs-lookup"><span data-stu-id="244c6-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="244c6-122">Es stellt das Basis 64-codierte Zertifikat dar.</span><span class="sxs-lookup"><span data-stu-id="244c6-122">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="244c6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="244c6-123">-DefaultProfile</span></span>
<span data-ttu-id="244c6-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="244c6-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="244c6-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="244c6-125">-DisplayName</span></span>
<span data-ttu-id="244c6-126">Der Anzeigename der neuen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="244c6-126">Display name of the new application.</span></span>

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

### <span data-ttu-id="244c6-127">-Enddate</span><span class="sxs-lookup"><span data-stu-id="244c6-127">-EndDate</span></span>
<span data-ttu-id="244c6-128">Das effektive Enddatum der Anmelde Informationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="244c6-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="244c6-129">Der Standardwert für Enddatum beträgt ein Jahr ab heute.</span><span class="sxs-lookup"><span data-stu-id="244c6-129">The default end date value is one year from today.</span></span> <span data-ttu-id="244c6-130">Bei einer "asymmetrischen" Art von Anmeldeinformationen muss dies auf ein oder vor dem Datum festgesetzt werden, an dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="244c6-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="244c6-131">-Startseite</span><span class="sxs-lookup"><span data-stu-id="244c6-131">-HomePage</span></span>
<span data-ttu-id="244c6-132">Die URL zur Startseite der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="244c6-132">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="244c6-133">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="244c6-133">-IdentifierUris</span></span>
<span data-ttu-id="244c6-134">Die URIs, die die Anwendung identifizieren.</span><span class="sxs-lookup"><span data-stu-id="244c6-134">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="244c6-135">-Keycredentials</span><span class="sxs-lookup"><span data-stu-id="244c6-135">-KeyCredentials</span></span>
<span data-ttu-id="244c6-136">Die Liste der Zertifikatanmeldeinformationen, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="244c6-136">The list of certificate credentials associated with the application.</span></span>

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

### <span data-ttu-id="244c6-137">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="244c6-137">-Password</span></span>
<span data-ttu-id="244c6-138">Das Kennwort, das der Anwendung zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="244c6-138">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="244c6-139">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="244c6-139">-PasswordCredentials</span></span>
<span data-ttu-id="244c6-140">Die Liste der Kennwortanmeldeinformationen, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="244c6-140">The list of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="244c6-141">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="244c6-141">-ReplyUrls</span></span>
<span data-ttu-id="244c6-142">Die URL der Anwendungsantwort.</span><span class="sxs-lookup"><span data-stu-id="244c6-142">The application reply urls.</span></span>

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

### <span data-ttu-id="244c6-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="244c6-143">-StartDate</span></span>
<span data-ttu-id="244c6-144">Der effektive Anfangstermin der Anmelde Informationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="244c6-144">The effective start date of the credential usage.</span></span>
<span data-ttu-id="244c6-145">Der Standardwert für das Anfangsdatum ist heute.</span><span class="sxs-lookup"><span data-stu-id="244c6-145">The default start date value is today.</span></span> <span data-ttu-id="244c6-146">Bei einer "asymmetrischen" Art von Anmeldeinformationen muss dies auf ein oder nach dem Datum festgesetzt werden, ab dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="244c6-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="244c6-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="244c6-147">-Confirm</span></span>
<span data-ttu-id="244c6-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="244c6-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="244c6-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="244c6-149">-WhatIf</span></span>
<span data-ttu-id="244c6-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="244c6-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="244c6-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="244c6-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="244c6-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="244c6-152">CommonParameters</span></span>
<span data-ttu-id="244c6-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="244c6-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="244c6-154">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="244c6-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="244c6-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="244c6-155">INPUTS</span></span>

### <span data-ttu-id="244c6-156">System. String</span><span class="sxs-lookup"><span data-stu-id="244c6-156">System.String</span></span>

### <span data-ttu-id="244c6-157">System. String []</span><span class="sxs-lookup"><span data-stu-id="244c6-157">System.String[]</span></span>

### <span data-ttu-id="244c6-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="244c6-158">System.Boolean</span></span>

### <span data-ttu-id="244c6-159">Microsoft. Azure. Commands. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="244c6-159">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="244c6-160">Microsoft. Azure. Commands. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="244c6-160">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="244c6-161">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="244c6-161">System.Security.SecureString</span></span>

### <span data-ttu-id="244c6-162">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="244c6-162">System.DateTime</span></span>

## <span data-ttu-id="244c6-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="244c6-163">OUTPUTS</span></span>

### <span data-ttu-id="244c6-164">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="244c6-164">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="244c6-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="244c6-165">NOTES</span></span>
<span data-ttu-id="244c6-166">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="244c6-166">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="244c6-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="244c6-167">RELATED LINKS</span></span>

[<span data-ttu-id="244c6-168">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="244c6-168">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="244c6-169">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="244c6-169">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="244c6-170">Neu – AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="244c6-170">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="244c6-171">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="244c6-171">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="244c6-172">Neu – AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="244c6-172">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="244c6-173">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="244c6-173">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

