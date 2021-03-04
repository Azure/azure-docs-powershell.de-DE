---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
ms.openlocfilehash: 1a80a5a2b6bb5e7af4d6467414feb3936377ea8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935507"
---
# <span data-ttu-id="b32cd-101">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="b32cd-101">New-AzADAppCredential</span></span>

## <span data-ttu-id="b32cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b32cd-102">SYNOPSIS</span></span>
<span data-ttu-id="b32cd-103">Fügt einer vorhandenen Anwendung eine Anmeldeinformationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="b32cd-103">Adds a credential to an existing application.</span></span>

## <span data-ttu-id="b32cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b32cd-104">SYNTAX</span></span>

### <span data-ttu-id="b32cd-105">ApplicationObjectIdWithPasswordParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b32cd-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADAppCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b32cd-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="b32cd-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b32cd-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="b32cd-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b32cd-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="b32cd-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b32cd-109">DisplayNameWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="b32cd-109">DisplayNameWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b32cd-110">DisplayNameWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="b32cd-110">DisplayNameWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b32cd-111">ApplicationObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="b32cd-111">ApplicationObjectWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b32cd-112">ApplicationObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="b32cd-112">ApplicationObjectWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b32cd-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b32cd-113">DESCRIPTION</span></span>
<span data-ttu-id="b32cd-114">Das New-AzADAppCredential-Cmdlet kann zum Hinzufügen neuer Anmeldeinformationen oder zum Rollup von Anmeldeinformationen für eine Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b32cd-114">The New-AzADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="b32cd-115">Die Anwendung wird durch Angabe der Anwendungsobjekt-ID oder der Anwendungs-ID identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b32cd-115">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="b32cd-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b32cd-116">EXAMPLES</span></span>

### <span data-ttu-id="b32cd-117">Beispiel 1: Erstellen einer neuen Anmeldeinformationen für eine Anwendung mithilfe eines Kennworts</span><span class="sxs-lookup"><span data-stu-id="b32cd-117">Example 1 - Create a new application credential using a password</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="b32cd-118">Der vorhandenen Anwendung mit der Objekt-ID '1f89cf81-0146-4f4e-beae-2007d0668416' wird ein neues Kennwort hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b32cd-118">A new password credential is added to the existing application with object id '1f89cf81-0146-4f4e-beae-2007d0668416'.</span></span>

### <span data-ttu-id="b32cd-119">Beispiel 2: Erstellen einer neuen Anmeldeinformationen für eine Anwendung mithilfe eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="b32cd-119">Example 2 - Create a new application credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="b32cd-120">Das bereitgestellte base64-codierte öffentliche X509-Zertifikat ("myapp.cer") wird der vorhandenen Anwendung mit der Anwendungs-ID '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58' hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b32cd-120">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="b32cd-121">Beispiel 3: Erstellen einer neuen Anmeldeinformationen für eine Anwendung mithilfe von Piping</span><span class="sxs-lookup"><span data-stu-id="b32cd-121">Example 3 - Create a new application credential using piping</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> Get-AzADApplication -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 | New-AzADAppCredential -Password $SecureStringPassword
```

<span data-ttu-id="b32cd-122">Ruft die Anwendung mit der Objekt-ID "1f89cf81-0146-4f4e-beae-2007d0668416" ab und gibt diese an die New-AzADAppCredential weiter, um eine neue Anmeldeinformationen für diese Anwendung mit dem angegebenen Kennwort zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b32cd-122">Gets the application with object id '1f89cf81-0146-4f4e-beae-2007d0668416' and pipes that to the New-AzADAppCredential to create a new application credential for that application with the given password.</span></span>

## <span data-ttu-id="b32cd-123">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b32cd-123">PARAMETERS</span></span>

### <span data-ttu-id="b32cd-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b32cd-124">-ApplicationId</span></span>
<span data-ttu-id="b32cd-125">Die Anwendungs-ID der Anwendung, der die Anmeldeinformationen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b32cd-125">The application id of the application to add the credentials to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithCertValueParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b32cd-126">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="b32cd-126">-ApplicationObject</span></span>
<span data-ttu-id="b32cd-127">Das Anwendungsobjekt, dem die Anmeldeinformationen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b32cd-127">The application object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithCertValueParameterSet, ApplicationObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b32cd-128">-CertValue</span><span class="sxs-lookup"><span data-stu-id="b32cd-128">-CertValue</span></span>
<span data-ttu-id="b32cd-129">Der Wert des "asymmetrischen" Anmeldeinformationstyps.</span><span class="sxs-lookup"><span data-stu-id="b32cd-129">The value of the "asymmetric" credential type.</span></span> <span data-ttu-id="b32cd-130">Es stellt das 64-codierte Basiszertifikat dar.</span><span class="sxs-lookup"><span data-stu-id="b32cd-130">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithCertValueParameterSet, ApplicationIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithCertValueParameterSet, ApplicationObjectWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b32cd-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b32cd-131">-DefaultProfile</span></span>
<span data-ttu-id="b32cd-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b32cd-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b32cd-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b32cd-133">-DisplayName</span></span>
<span data-ttu-id="b32cd-134">Der Anzeigename der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b32cd-134">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithPasswordParameterSet, DisplayNameWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b32cd-135">-EndDate</span><span class="sxs-lookup"><span data-stu-id="b32cd-135">-EndDate</span></span>
<span data-ttu-id="b32cd-136">Das effektive Enddatum der Anmeldeinformationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="b32cd-136">The effective end date of the credential usage.</span></span> <span data-ttu-id="b32cd-137">Der Standardwert für das Enddatum ist ein Jahr ab heute.</span><span class="sxs-lookup"><span data-stu-id="b32cd-137">The default end date value is one year from today.</span></span>  <span data-ttu-id="b32cd-138">Bei "asymmetrischen" Typanmeldeinformationen muss dies auf am oder vor dem Datum festgelegt sein, an dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="b32cd-138">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b32cd-139">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b32cd-139">-ObjectId</span></span>
<span data-ttu-id="b32cd-140">Die Objekt-ID der Anwendung, der die Anmeldeinformationen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b32cd-140">The object id of the application to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationObjectIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b32cd-141">-Password</span><span class="sxs-lookup"><span data-stu-id="b32cd-141">-Password</span></span>
<span data-ttu-id="b32cd-142">Das Kennwort, das der Anwendung zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b32cd-142">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: DisplayNameWithPasswordParameterSet, ApplicationObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b32cd-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="b32cd-143">-StartDate</span></span>
<span data-ttu-id="b32cd-144">Das effektive Startdatum der Anmeldeinformationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="b32cd-144">The effective start date of the credential usage.</span></span> <span data-ttu-id="b32cd-145">Der Standardwert für das Startdatum ist heute.</span><span class="sxs-lookup"><span data-stu-id="b32cd-145">The default start date value is today.</span></span> <span data-ttu-id="b32cd-146">Bei "asymmetrischen" Typanmeldeinformationen muss dies auf am oder nach dem Datum festgelegt sein, ab dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="b32cd-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b32cd-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b32cd-147">-Confirm</span></span>
<span data-ttu-id="b32cd-148">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b32cd-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b32cd-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b32cd-149">-WhatIf</span></span>
<span data-ttu-id="b32cd-150">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b32cd-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b32cd-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b32cd-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b32cd-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b32cd-152">CommonParameters</span></span>
<span data-ttu-id="b32cd-153">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b32cd-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b32cd-154">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b32cd-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b32cd-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b32cd-155">INPUTS</span></span>

### <span data-ttu-id="b32cd-156">System.String</span><span class="sxs-lookup"><span data-stu-id="b32cd-156">System.String</span></span>

### <span data-ttu-id="b32cd-157">System.Guid</span><span class="sxs-lookup"><span data-stu-id="b32cd-157">System.Guid</span></span>

### <span data-ttu-id="b32cd-158">Microsoft.Azure.Commands.ActiveDirectory.PSDApplication</span><span class="sxs-lookup"><span data-stu-id="b32cd-158">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="b32cd-159">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="b32cd-159">System.Security.SecureString</span></span>

### <span data-ttu-id="b32cd-160">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="b32cd-160">System.DateTime</span></span>

## <span data-ttu-id="b32cd-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b32cd-161">OUTPUTS</span></span>

### <span data-ttu-id="b32cd-162">Microsoft.Azure.Commands.ActiveDirectory.PSDCredential</span><span class="sxs-lookup"><span data-stu-id="b32cd-162">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="b32cd-163">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b32cd-163">NOTES</span></span>

## <span data-ttu-id="b32cd-164">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b32cd-164">RELATED LINKS</span></span>

[<span data-ttu-id="b32cd-165">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="b32cd-165">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="b32cd-166">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="b32cd-166">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="b32cd-167">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="b32cd-167">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

