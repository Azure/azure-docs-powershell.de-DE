---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
ms.openlocfilehash: 171f09e2d9a9e6e646731817526451b311f94482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500418"
---
# <span data-ttu-id="6c014-101">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="6c014-101">New-AzureRmADApplication</span></span>

## <span data-ttu-id="6c014-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6c014-102">SYNOPSIS</span></span>
<span data-ttu-id="6c014-103">Erstellt eine neue Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6c014-103">Creates a new azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c014-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c014-104">SYNTAX</span></span>

### <span data-ttu-id="6c014-105">ApplicationWithoutCredentialParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6c014-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c014-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c014-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c014-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c014-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c014-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c014-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c014-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c014-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c014-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c014-110">DESCRIPTION</span></span>
<span data-ttu-id="6c014-111">Erstellt eine neue Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6c014-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="6c014-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c014-112">EXAMPLES</span></span>

### <span data-ttu-id="6c014-113">Erstellen Sie eine neue Aad-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6c014-113">Create new AAD application.</span></span>
```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="6c014-114">Erstellt eine neue Azure Active Directory-Anwendung ohne Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="6c014-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="6c014-115">Erstellen Sie eine neue Aad-Anwendung mit einem Kennwort.</span><span class="sxs-lookup"><span data-stu-id="6c014-115">Create new AAD application with password.</span></span>
```
PS E:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="6c014-116">Erstellt eine neue Azure Active Directory-Anwendung und ordnet dem Kennwort Anmeldeinformationen zu.</span><span class="sxs-lookup"><span data-stu-id="6c014-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="6c014-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c014-117">PARAMETERS</span></span>

### <span data-ttu-id="6c014-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="6c014-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="6c014-119">Der Wert, der angibt, ob es sich bei der Anwendung um einen einzelnen Mandanten oder um einen Mandanten handelt.</span><span class="sxs-lookup"><span data-stu-id="6c014-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c014-120">-Certvalue</span><span class="sxs-lookup"><span data-stu-id="6c014-120">-CertValue</span></span>
<span data-ttu-id="6c014-121">Der Wert des Anmeldeinformationstyps "asymmetrisch".</span><span class="sxs-lookup"><span data-stu-id="6c014-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="6c014-122">Es stellt das Basis 64-codierte Zertifikat dar.</span><span class="sxs-lookup"><span data-stu-id="6c014-122">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c014-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c014-123">-DefaultProfile</span></span>
<span data-ttu-id="6c014-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6c014-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c014-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6c014-125">-DisplayName</span></span>
<span data-ttu-id="6c014-126">Der Anzeigename der neuen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6c014-126">Display name of the new application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c014-127">-Enddate</span><span class="sxs-lookup"><span data-stu-id="6c014-127">-EndDate</span></span>
<span data-ttu-id="6c014-128">Das effektive Enddatum der Anmelde Informationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="6c014-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="6c014-129">Der Standardwert für Enddatum beträgt ein Jahr ab heute.</span><span class="sxs-lookup"><span data-stu-id="6c014-129">The default end date value is one year from today.</span></span> <span data-ttu-id="6c014-130">Bei einer "asymmetrischen" Art von Anmeldeinformationen muss dies auf ein oder vor dem Datum festgesetzt werden, an dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="6c014-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c014-131">-Startseite</span><span class="sxs-lookup"><span data-stu-id="6c014-131">-HomePage</span></span>
<span data-ttu-id="6c014-132">Die URL zur Startseite der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6c014-132">The URL to the application homepage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c014-133">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="6c014-133">-IdentifierUris</span></span>
<span data-ttu-id="6c014-134">Die URIs, die die Anwendung identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6c014-134">The URIs that identify the application.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c014-135">-Keycredentials</span><span class="sxs-lookup"><span data-stu-id="6c014-135">-KeyCredentials</span></span>
<span data-ttu-id="6c014-136">Die Liste der Zertifikatanmeldeinformationen, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6c014-136">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c014-137">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="6c014-137">-Password</span></span>
<span data-ttu-id="6c014-138">Das Kennwort, das der Anwendung zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6c014-138">The password to be associated with the application.</span></span>

```yaml
Type: SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c014-139">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="6c014-139">-PasswordCredentials</span></span>
<span data-ttu-id="6c014-140">Die Liste der Kennwortanmeldeinformationen, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6c014-140">The list of password credentials associated with the application.</span></span>

```yaml
Type: PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c014-141">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="6c014-141">-ReplyUrls</span></span>
<span data-ttu-id="6c014-142">Die URL der Anwendungsantwort.</span><span class="sxs-lookup"><span data-stu-id="6c014-142">The application reply urls.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c014-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="6c014-143">-StartDate</span></span>
<span data-ttu-id="6c014-144">Der effektive Anfangstermin der Anmelde Informationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="6c014-144">The effective start date of the credential usage.</span></span>
<span data-ttu-id="6c014-145">Der Standardwert für das Anfangsdatum ist heute.</span><span class="sxs-lookup"><span data-stu-id="6c014-145">The default start date value is today.</span></span> <span data-ttu-id="6c014-146">Bei einer "asymmetrischen" Art von Anmeldeinformationen muss dies auf ein oder nach dem Datum festgesetzt werden, ab dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="6c014-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c014-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6c014-147">-Confirm</span></span>
<span data-ttu-id="6c014-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6c014-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c014-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c014-149">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c014-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c014-150">CommonParameters</span></span>
<span data-ttu-id="6c014-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c014-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c014-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c014-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c014-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6c014-153">INPUTS</span></span>

### <span data-ttu-id="6c014-154">Keine</span><span class="sxs-lookup"><span data-stu-id="6c014-154">None</span></span>
<span data-ttu-id="6c014-155">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="6c014-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6c014-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6c014-156">OUTPUTS</span></span>

### <span data-ttu-id="6c014-157">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="6c014-157">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="6c014-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="6c014-158">NOTES</span></span>
<span data-ttu-id="6c014-159">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="6c014-159">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="6c014-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6c014-160">RELATED LINKS</span></span>

[<span data-ttu-id="6c014-161">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="6c014-161">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="6c014-162">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="6c014-162">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="6c014-163">Neu – AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6c014-163">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="6c014-164">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="6c014-164">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="6c014-165">Neu – AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="6c014-165">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="6c014-166">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="6c014-166">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

