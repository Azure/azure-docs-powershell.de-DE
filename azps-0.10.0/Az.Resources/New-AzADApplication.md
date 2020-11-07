---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADApplication.md
ms.openlocfilehash: 3850e5f142e7ec1496ace1225ab53c160794775a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843380"
---
# <span data-ttu-id="e8263-101">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="e8263-101">New-AzADApplication</span></span>

## <span data-ttu-id="e8263-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e8263-102">SYNOPSIS</span></span>
<span data-ttu-id="e8263-103">Erstellt eine neue Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e8263-103">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="e8263-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8263-104">SYNTAX</span></span>

### <span data-ttu-id="e8263-105">ApplicationWithoutCredentialParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e8263-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8263-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8263-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8263-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8263-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8263-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8263-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8263-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8263-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8263-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8263-110">DESCRIPTION</span></span>
<span data-ttu-id="e8263-111">Erstellt eine neue Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e8263-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="e8263-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e8263-112">EXAMPLES</span></span>

### <span data-ttu-id="e8263-113">Beispiel 1: Erstellen einer neuen Aad-Anwendung</span><span class="sxs-lookup"><span data-stu-id="e8263-113">Example 1 - Create new AAD application.</span></span>

```
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="e8263-114">Erstellt eine neue Azure Active Directory-Anwendung ohne Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="e8263-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="e8263-115">Beispiel 2: Erstellen einer neuen Aad-Anwendung mit einem Kennwort</span><span class="sxs-lookup"><span data-stu-id="e8263-115">Example 2 - Create new AAD application with password.</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="e8263-116">Erstellt eine neue Azure Active Directory-Anwendung und ordnet dem Kennwort Anmeldeinformationen zu.</span><span class="sxs-lookup"><span data-stu-id="e8263-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="e8263-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8263-117">PARAMETERS</span></span>

### <span data-ttu-id="e8263-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="e8263-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="e8263-119">Der Wert, der angibt, ob es sich bei der Anwendung um einen einzelnen Mandanten oder um einen Mandanten handelt.</span><span class="sxs-lookup"><span data-stu-id="e8263-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

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

### <span data-ttu-id="e8263-120">-Certvalue</span><span class="sxs-lookup"><span data-stu-id="e8263-120">-CertValue</span></span>
<span data-ttu-id="e8263-121">Der Wert des Anmeldeinformationstyps "asymmetrisch".</span><span class="sxs-lookup"><span data-stu-id="e8263-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="e8263-122">Es stellt das Basis 64-codierte Zertifikat dar.</span><span class="sxs-lookup"><span data-stu-id="e8263-122">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="e8263-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8263-123">-DefaultProfile</span></span>
<span data-ttu-id="e8263-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e8263-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8263-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e8263-125">-DisplayName</span></span>
<span data-ttu-id="e8263-126">Der Anzeigename der neuen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e8263-126">Display name of the new application.</span></span>

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

### <span data-ttu-id="e8263-127">-Enddate</span><span class="sxs-lookup"><span data-stu-id="e8263-127">-EndDate</span></span>
<span data-ttu-id="e8263-128">Das effektive Enddatum der Anmelde Informationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="e8263-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="e8263-129">Der Standardwert für Enddatum beträgt ein Jahr ab heute.</span><span class="sxs-lookup"><span data-stu-id="e8263-129">The default end date value is one year from today.</span></span> <span data-ttu-id="e8263-130">Bei einer "asymmetrischen" Art von Anmeldeinformationen muss dies auf ein oder vor dem Datum festgesetzt werden, an dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="e8263-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="e8263-131">-Startseite</span><span class="sxs-lookup"><span data-stu-id="e8263-131">-HomePage</span></span>
<span data-ttu-id="e8263-132">Die URL zur Startseite der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e8263-132">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="e8263-133">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="e8263-133">-IdentifierUris</span></span>
<span data-ttu-id="e8263-134">Die URIs, die die Anwendung identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e8263-134">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="e8263-135">-Keycredentials</span><span class="sxs-lookup"><span data-stu-id="e8263-135">-KeyCredentials</span></span>
<span data-ttu-id="e8263-136">Die Liste der Zertifikatanmeldeinformationen, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e8263-136">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8263-137">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="e8263-137">-Password</span></span>
<span data-ttu-id="e8263-138">Das Kennwort, das der Anwendung zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8263-138">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="e8263-139">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="e8263-139">-PasswordCredentials</span></span>
<span data-ttu-id="e8263-140">Die Liste der Kennwortanmeldeinformationen, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e8263-140">The list of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8263-141">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="e8263-141">-ReplyUrls</span></span>
<span data-ttu-id="e8263-142">Die URL der Anwendungsantwort.</span><span class="sxs-lookup"><span data-stu-id="e8263-142">The application reply urls.</span></span>

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

### <span data-ttu-id="e8263-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="e8263-143">-StartDate</span></span>
<span data-ttu-id="e8263-144">Der effektive Anfangstermin der Anmelde Informationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="e8263-144">The effective start date of the credential usage.</span></span>
<span data-ttu-id="e8263-145">Der Standardwert für das Anfangsdatum ist heute.</span><span class="sxs-lookup"><span data-stu-id="e8263-145">The default start date value is today.</span></span> <span data-ttu-id="e8263-146">Bei einer "asymmetrischen" Art von Anmeldeinformationen muss dies auf ein oder nach dem Datum festgesetzt werden, ab dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="e8263-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="e8263-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e8263-147">-Confirm</span></span>
<span data-ttu-id="e8263-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e8263-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8263-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8263-149">-WhatIf</span></span>
<span data-ttu-id="e8263-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e8263-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8263-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e8263-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8263-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8263-152">CommonParameters</span></span>
<span data-ttu-id="e8263-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8263-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8263-154">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8263-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8263-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e8263-155">INPUTS</span></span>

### <span data-ttu-id="e8263-156">System. String</span><span class="sxs-lookup"><span data-stu-id="e8263-156">System.String</span></span>

### <span data-ttu-id="e8263-157">System. String []</span><span class="sxs-lookup"><span data-stu-id="e8263-157">System.String[]</span></span>

### <span data-ttu-id="e8263-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e8263-158">System.Boolean</span></span>

### <span data-ttu-id="e8263-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="e8263-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="e8263-160">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="e8263-160">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="e8263-161">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="e8263-161">System.Security.SecureString</span></span>

### <span data-ttu-id="e8263-162">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="e8263-162">System.DateTime</span></span>

## <span data-ttu-id="e8263-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e8263-163">OUTPUTS</span></span>

### <span data-ttu-id="e8263-164">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="e8263-164">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="e8263-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="e8263-165">NOTES</span></span>
<span data-ttu-id="e8263-166">Schlüsselwörter: Azure, AZ, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="e8263-166">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="e8263-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e8263-167">RELATED LINKS</span></span>

[<span data-ttu-id="e8263-168">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="e8263-168">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="e8263-169">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="e8263-169">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="e8263-170">Neu – AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e8263-170">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="e8263-171">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e8263-171">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="e8263-172">Neu – AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e8263-172">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="e8263-173">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e8263-173">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

