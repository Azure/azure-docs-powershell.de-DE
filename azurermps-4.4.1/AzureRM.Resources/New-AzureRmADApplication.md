---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
ms.openlocfilehash: c43bba247268d7ffcdbc2c33d7198415738c5694
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504762"
---
# <span data-ttu-id="08ada-101">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="08ada-101">New-AzureRmADApplication</span></span>

## <span data-ttu-id="08ada-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="08ada-102">SYNOPSIS</span></span>
<span data-ttu-id="08ada-103">Erstellt eine neue Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="08ada-103">Creates a new azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08ada-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="08ada-104">SYNTAX</span></span>

### <span data-ttu-id="08ada-105">ApplicationWithoutCredentialParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="08ada-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08ada-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="08ada-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08ada-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="08ada-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08ada-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="08ada-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08ada-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="08ada-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08ada-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08ada-110">DESCRIPTION</span></span>
<span data-ttu-id="08ada-111">Erstellt eine neue Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="08ada-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="08ada-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08ada-112">EXAMPLES</span></span>

### <span data-ttu-id="08ada-113">--------------------------Erstellen Sie eine neue Aad-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="08ada-113">--------------------------  Create new AAD application.</span></span>  --------------------------
```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="08ada-114">Erstellt eine neue Azure Active Directory-Anwendung ohne Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="08ada-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="08ada-115">--------------------------Neue Aad-Anwendung mit Kennwort erstellen.</span><span class="sxs-lookup"><span data-stu-id="08ada-115">--------------------------  Create new AAD application with password.</span></span>  --------------------------
```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password "password"
```

<span data-ttu-id="08ada-116">Erstellt eine neue Azure Active Directory-Anwendung und ordnet dem Kennwort Anmeldeinformationen zu.</span><span class="sxs-lookup"><span data-stu-id="08ada-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="08ada-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="08ada-117">PARAMETERS</span></span>

### <span data-ttu-id="08ada-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="08ada-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="08ada-119">Der Wert, der angibt, ob es sich bei der Anwendung um einen einzelnen Mandanten oder um einen Mandanten handelt.</span><span class="sxs-lookup"><span data-stu-id="08ada-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

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

### <span data-ttu-id="08ada-120">-Certvalue</span><span class="sxs-lookup"><span data-stu-id="08ada-120">-CertValue</span></span>
<span data-ttu-id="08ada-121">Der Wert des Anmeldeinformationstyps "asymmetrisch".</span><span class="sxs-lookup"><span data-stu-id="08ada-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="08ada-122">Es stellt das Basis 64-codierte Zertifikat dar.</span><span class="sxs-lookup"><span data-stu-id="08ada-122">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="08ada-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="08ada-123">-DisplayName</span></span>
<span data-ttu-id="08ada-124">Der Anzeigename der neuen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="08ada-124">Display name of the new application.</span></span>

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

### <span data-ttu-id="08ada-125">-Enddate</span><span class="sxs-lookup"><span data-stu-id="08ada-125">-EndDate</span></span>
<span data-ttu-id="08ada-126">Das effektive Enddatum der Anmelde Informationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="08ada-126">The effective end date of the credential usage.</span></span>
<span data-ttu-id="08ada-127">Der Standardwert für Enddatum beträgt ein Jahr ab heute.</span><span class="sxs-lookup"><span data-stu-id="08ada-127">The default end date value is one year from today.</span></span> <span data-ttu-id="08ada-128">Bei einer "asymmetrischen" Art von Anmeldeinformationen muss dies auf ein oder vor dem Datum festgesetzt werden, an dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="08ada-128">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="08ada-129">-Startseite</span><span class="sxs-lookup"><span data-stu-id="08ada-129">-HomePage</span></span>
<span data-ttu-id="08ada-130">Die URL zur Startseite der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="08ada-130">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="08ada-131">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="08ada-131">-IdentifierUris</span></span>
<span data-ttu-id="08ada-132">Die URIs, die die Anwendung identifizieren.</span><span class="sxs-lookup"><span data-stu-id="08ada-132">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="08ada-133">-Keycredentials</span><span class="sxs-lookup"><span data-stu-id="08ada-133">-KeyCredentials</span></span>
<span data-ttu-id="08ada-134">Die Liste der Zertifikatanmeldeinformationen, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="08ada-134">The list of certificate credentials associated with the application.</span></span>

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

### <span data-ttu-id="08ada-135">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="08ada-135">-Password</span></span>
<span data-ttu-id="08ada-136">Das Kennwort, das der Anwendung zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="08ada-136">The password to be associated with the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithPasswordPlainParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08ada-137">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="08ada-137">-PasswordCredentials</span></span>
<span data-ttu-id="08ada-138">Die Liste der Kennwortanmeldeinformationen, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="08ada-138">The list of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="08ada-139">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="08ada-139">-ReplyUrls</span></span>
<span data-ttu-id="08ada-140">Die URL der Anwendungsantwort.</span><span class="sxs-lookup"><span data-stu-id="08ada-140">The application reply urls.</span></span>

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

### <span data-ttu-id="08ada-141">-StartDate</span><span class="sxs-lookup"><span data-stu-id="08ada-141">-StartDate</span></span>
<span data-ttu-id="08ada-142">Der effektive Anfangstermin der Anmelde Informationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="08ada-142">The effective start date of the credential usage.</span></span>
<span data-ttu-id="08ada-143">Der Standardwert für das Anfangsdatum ist heute.</span><span class="sxs-lookup"><span data-stu-id="08ada-143">The default start date value is today.</span></span> <span data-ttu-id="08ada-144">Bei einer "asymmetrischen" Art von Anmeldeinformationen muss dies auf ein oder nach dem Datum festgesetzt werden, ab dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="08ada-144">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="08ada-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="08ada-145">-Confirm</span></span>
<span data-ttu-id="08ada-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="08ada-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08ada-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08ada-147">-WhatIf</span></span>
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

### <span data-ttu-id="08ada-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08ada-148">-DefaultProfile</span></span>
<span data-ttu-id="08ada-149">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="08ada-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08ada-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08ada-150">CommonParameters</span></span>
<span data-ttu-id="08ada-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08ada-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08ada-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08ada-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08ada-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="08ada-153">INPUTS</span></span>

## <span data-ttu-id="08ada-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="08ada-154">OUTPUTS</span></span>

### <span data-ttu-id="08ada-155">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="08ada-155">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="08ada-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="08ada-156">NOTES</span></span>
<span data-ttu-id="08ada-157">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="08ada-157">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="08ada-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="08ada-158">RELATED LINKS</span></span>

[<span data-ttu-id="08ada-159">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="08ada-159">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="08ada-160">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="08ada-160">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="08ada-161">Neu – AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="08ada-161">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="08ada-162">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="08ada-162">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="08ada-163">Neu – AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="08ada-163">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="08ada-164">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="08ada-164">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

