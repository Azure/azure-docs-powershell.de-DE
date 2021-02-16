---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
ms.openlocfilehash: 8290ad3779c91565509833bbf41d7f9b37b07635
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153681"
---
# <span data-ttu-id="4348f-101">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="4348f-101">New-AzADAppCredential</span></span>

## <span data-ttu-id="4348f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4348f-102">SYNOPSIS</span></span>
<span data-ttu-id="4348f-103">Fügt einer vorhandenen Anwendung Anmeldeinformationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="4348f-103">Adds a credential to an existing application.</span></span>

## <span data-ttu-id="4348f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4348f-104">SYNTAX</span></span>

### <span data-ttu-id="4348f-105">ApplicationObjectIdWithPasswordParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4348f-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADAppCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4348f-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="4348f-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4348f-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="4348f-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4348f-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="4348f-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4348f-109">DisplayNameWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="4348f-109">DisplayNameWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4348f-110">DisplayNameWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="4348f-110">DisplayNameWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4348f-111">ApplicationObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="4348f-111">ApplicationObjectWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4348f-112">ApplicationObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="4348f-112">ApplicationObjectWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4348f-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4348f-113">DESCRIPTION</span></span>
<span data-ttu-id="4348f-114">Das New-AzADAppCredential cmdlet kann zum Hinzufügen neuer Anmeldeinformationen oder zum Roll von Anmeldeinformationen für eine Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4348f-114">The New-AzADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="4348f-115">Die Anwendung wird durch Angabe der Anwendungsobjekt-ID oder Anwendungs-ID identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4348f-115">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="4348f-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4348f-116">EXAMPLES</span></span>

### <span data-ttu-id="4348f-117">Beispiel 1: Erstellen einer neuen Anmeldeinformationen für eine Anwendung mithilfe eines Kennworts</span><span class="sxs-lookup"><span data-stu-id="4348f-117">Example 1 - Create a new application credential using a password</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="4348f-118">Der vorhandenen Anwendung wird ein neues Kennwort mit der Objekt-ID '1f89cf81-0146-4f4e-beae-2007d0668416' hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4348f-118">A new password credential is added to the existing application with object id '1f89cf81-0146-4f4e-beae-2007d0668416'.</span></span>

### <span data-ttu-id="4348f-119">Beispiel 2: Erstellen einer neuen Anmeldeinformationen für eine Anwendung mithilfe eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="4348f-119">Example 2 - Create a new application credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="4348f-120">Das bereitgestellte base64-codierte öffentliche X509-Zertifikat ("myapp.cer") wird der vorhandenen Anwendung mit der Anwendungs-ID '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58' hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4348f-120">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="4348f-121">Beispiel 3: Erstellen einer neuen Anmeldeinformationen für eine Anwendung mithilfe der Piping</span><span class="sxs-lookup"><span data-stu-id="4348f-121">Example 3 - Create a new application credential using piping</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> Get-AzADApplication -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 | New-AzADAppCredential -Password $SecureStringPassword
```

<span data-ttu-id="4348f-122">Ruft die Anwendung mit der Objekt-ID '1f89cf81-0146-4f4e-beae-2007d0668416' ab und gibt diese an die New-AzADAppCredential weiter, um eine neue Anmeldeinformationen für die Anwendung mit dem angegebenen Kennwort zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4348f-122">Gets the application with object id '1f89cf81-0146-4f4e-beae-2007d0668416' and pipes that to the New-AzADAppCredential to create a new application credential for that application with the given password.</span></span>

## <span data-ttu-id="4348f-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4348f-123">PARAMETERS</span></span>

### <span data-ttu-id="4348f-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="4348f-124">-ApplicationId</span></span>
<span data-ttu-id="4348f-125">Die Anwendungs-ID der Anwendung, der die Anmeldeinformationen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="4348f-125">The application id of the application to add the credentials to.</span></span>

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

### <span data-ttu-id="4348f-126">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="4348f-126">-ApplicationObject</span></span>
<span data-ttu-id="4348f-127">Das Anwendungsobjekt, dem die Anmeldeinformationen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="4348f-127">The application object to add the credentials to.</span></span>

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

### <span data-ttu-id="4348f-128">-CertValue</span><span class="sxs-lookup"><span data-stu-id="4348f-128">-CertValue</span></span>
<span data-ttu-id="4348f-129">Der Wert des "asymmetrischen" Anmeldeinformationstyps.</span><span class="sxs-lookup"><span data-stu-id="4348f-129">The value of the "asymmetric" credential type.</span></span> <span data-ttu-id="4348f-130">Es stellt das 64-codierte Basiszertifikat dar.</span><span class="sxs-lookup"><span data-stu-id="4348f-130">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="4348f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4348f-131">-DefaultProfile</span></span>
<span data-ttu-id="4348f-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4348f-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4348f-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4348f-133">-DisplayName</span></span>
<span data-ttu-id="4348f-134">Der Anzeigename der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="4348f-134">The display name of the application.</span></span>

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

### <span data-ttu-id="4348f-135">-EndDate</span><span class="sxs-lookup"><span data-stu-id="4348f-135">-EndDate</span></span>
<span data-ttu-id="4348f-136">Das Effektive Enddatum der Verwendung der Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="4348f-136">The effective end date of the credential usage.</span></span> <span data-ttu-id="4348f-137">Der Standardmäßige Enddatumswert liegt ein Jahr nach heute.</span><span class="sxs-lookup"><span data-stu-id="4348f-137">The default end date value is one year from today.</span></span>  <span data-ttu-id="4348f-138">Bei Anmeldeinformationen vom Typ "asymmetrischer Art" muss dies auf das Datum oder vor dem Datum festgelegt werden, an dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="4348f-138">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="4348f-139">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4348f-139">-ObjectId</span></span>
<span data-ttu-id="4348f-140">Die Objekt-ID der Anwendung, der die Anmeldeinformationen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="4348f-140">The object id of the application to add the credentials to.</span></span>

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

### <span data-ttu-id="4348f-141">-Password</span><span class="sxs-lookup"><span data-stu-id="4348f-141">-Password</span></span>
<span data-ttu-id="4348f-142">Das Kennwort, das der Anwendung zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4348f-142">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="4348f-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="4348f-143">-StartDate</span></span>
<span data-ttu-id="4348f-144">Das Effektive Startdatum der Verwendung der Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="4348f-144">The effective start date of the credential usage.</span></span> <span data-ttu-id="4348f-145">Der Standardwert für das Startdatum ist "Heute".</span><span class="sxs-lookup"><span data-stu-id="4348f-145">The default start date value is today.</span></span> <span data-ttu-id="4348f-146">Bei Anmeldeinformationen vom Typ "asymmetrischer Art" muss dies auf das Datum oder nach dem Datum festgelegt werden, ab dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="4348f-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="4348f-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4348f-147">-Confirm</span></span>
<span data-ttu-id="4348f-148">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4348f-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4348f-149">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4348f-149">-WhatIf</span></span>
<span data-ttu-id="4348f-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4348f-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4348f-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4348f-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4348f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4348f-152">CommonParameters</span></span>
<span data-ttu-id="4348f-153">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4348f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4348f-154">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4348f-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4348f-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4348f-155">INPUTS</span></span>

### <span data-ttu-id="4348f-156">System.String</span><span class="sxs-lookup"><span data-stu-id="4348f-156">System.String</span></span>

### <span data-ttu-id="4348f-157">System.Guid</span><span class="sxs-lookup"><span data-stu-id="4348f-157">System.Guid</span></span>

### <span data-ttu-id="4348f-158">Microsoft.Azure.Commands.ActiveDirectory.WERDENDApplication</span><span class="sxs-lookup"><span data-stu-id="4348f-158">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="4348f-159">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="4348f-159">System.Security.SecureString</span></span>

### <span data-ttu-id="4348f-160">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="4348f-160">System.DateTime</span></span>

## <span data-ttu-id="4348f-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4348f-161">OUTPUTS</span></span>

### <span data-ttu-id="4348f-162">Microsoft.Azure.Commands.ActiveDirectory.ODERDCredential</span><span class="sxs-lookup"><span data-stu-id="4348f-162">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="4348f-163">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4348f-163">NOTES</span></span>

## <span data-ttu-id="4348f-164">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4348f-164">RELATED LINKS</span></span>

[<span data-ttu-id="4348f-165">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="4348f-165">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="4348f-166">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="4348f-166">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="4348f-167">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="4348f-167">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

