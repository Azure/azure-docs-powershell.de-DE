---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
ms.openlocfilehash: 9305dc27f6c6486f34d1b5b9fb68844f967e3989
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659614"
---
# <span data-ttu-id="c4d0d-101">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c4d0d-101">New-AzADAppCredential</span></span>

## <span data-ttu-id="c4d0d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4d0d-102">SYNOPSIS</span></span>
<span data-ttu-id="c4d0d-103">Fügt eine Anmeldeinformationen zu einer vorhandenen Anwendung hinzu.</span><span class="sxs-lookup"><span data-stu-id="c4d0d-103">Adds a credential to an existing application.</span></span>

## <span data-ttu-id="c4d0d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4d0d-104">SYNTAX</span></span>

### <span data-ttu-id="c4d0d-105">ApplicationObjectIdWithPasswordParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c4d0d-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADAppCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4d0d-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4d0d-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4d0d-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4d0d-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4d0d-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4d0d-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4d0d-109">DisplayNameWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4d0d-109">DisplayNameWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4d0d-110">DisplayNameWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4d0d-110">DisplayNameWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4d0d-111">ApplicationObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4d0d-111">ApplicationObjectWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4d0d-112">ApplicationObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4d0d-112">ApplicationObjectWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4d0d-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4d0d-113">DESCRIPTION</span></span>
<span data-ttu-id="c4d0d-114">Mithilfe des New-AzADAppCredential-Cmdlets können Sie eine neue Anmeldeinformationen hinzufügen oder die Anmeldeinformationen für eine Anwendung Rollen.</span><span class="sxs-lookup"><span data-stu-id="c4d0d-114">The New-AzADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="c4d0d-115">Die Anwendung wird identifiziert, indem entweder die Anwendungsobjekt-ID oder die Anwendungs-ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c4d0d-115">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="c4d0d-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4d0d-116">EXAMPLES</span></span>

### <span data-ttu-id="c4d0d-117">Beispiel 1: Erstellen einer neuen Anwendungs Anmeldeinformationen mithilfe eines Kennworts</span><span class="sxs-lookup"><span data-stu-id="c4d0d-117">Example 1 - Create a new application credential using a password</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="c4d0d-118">Mit der Objekt-ID "1f89cf81-0146-4f4e-BEAE-2007d0668416" wird dem vorhandenen geschriebene eine neue kennwortberechtigung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c4d0d-118">A new password credential is added to the existing appplication with object id '1f89cf81-0146-4f4e-beae-2007d0668416'.</span></span>

### <span data-ttu-id="c4d0d-119">Beispiel 2: Erstellen einer neuen Anwendungs Anmeldeinformationen mithilfe eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="c4d0d-119">Example 2 - Create a new application credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="c4d0d-120">Das bereitgestellte Base64-codierte öffentliche X509-Zertifikat ("MyApp. cer") wird der vorhandenen Anwendung mit der Anwendungs-ID "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c4d0d-120">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="c4d0d-121">Beispiel 3: Erstellen einer neuen Anwendungs Anmeldeinformationen mithilfe von Piping</span><span class="sxs-lookup"><span data-stu-id="c4d0d-121">Example 3 - Create a new application credential using piping</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> Get-AzADApplication -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 | New-AzADAppCredential -Password $SecureStringPassword
```

<span data-ttu-id="c4d0d-122">Ruft die Anwendung mit der Objekt-ID "1f89cf81-0146-4f4e-BEAE-2007d0668416" und Pipes ab, die zum New-AzADAppCredential, um eine neue Anwendungs Anmeldeinformationen für diese Anwendung mit dem angegebenen Kennwort zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c4d0d-122">Gets the application with object id '1f89cf81-0146-4f4e-beae-2007d0668416' and pipes that to the New-AzADAppCredential to create a new application credential for that application with the given password.</span></span>

## <span data-ttu-id="c4d0d-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4d0d-123">PARAMETERS</span></span>

### <span data-ttu-id="c4d0d-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c4d0d-124">-ApplicationId</span></span>
<span data-ttu-id="c4d0d-125">Die Anwendungs-ID der Anwendung, der die Anmeldeinformationen hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c4d0d-125">The application id of the application to add the credentials to.</span></span>

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

### <span data-ttu-id="c4d0d-126">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="c4d0d-126">-ApplicationObject</span></span>
<span data-ttu-id="c4d0d-127">Das Application-Objekt, dem die Anmeldeinformationen hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c4d0d-127">The application object to add the credentials to.</span></span>

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

### <span data-ttu-id="c4d0d-128">-Certvalue</span><span class="sxs-lookup"><span data-stu-id="c4d0d-128">-CertValue</span></span>
<span data-ttu-id="c4d0d-129">Der Wert des Anmeldeinformationstyps "asymmetrisch".</span><span class="sxs-lookup"><span data-stu-id="c4d0d-129">The value of the "asymmetric" credential type.</span></span> <span data-ttu-id="c4d0d-130">Es stellt das Basis 64-codierte Zertifikat dar.</span><span class="sxs-lookup"><span data-stu-id="c4d0d-130">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="c4d0d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4d0d-131">-DefaultProfile</span></span>
<span data-ttu-id="c4d0d-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c4d0d-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4d0d-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c4d0d-133">-DisplayName</span></span>
<span data-ttu-id="c4d0d-134">Der Anzeigename der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c4d0d-134">The display name of the application.</span></span>

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

### <span data-ttu-id="c4d0d-135">-Enddate</span><span class="sxs-lookup"><span data-stu-id="c4d0d-135">-EndDate</span></span>
<span data-ttu-id="c4d0d-136">Das effektive Enddatum der Anmelde Informationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="c4d0d-136">The effective end date of the credential usage.</span></span> <span data-ttu-id="c4d0d-137">Der Standardwert für Enddatum beträgt ein Jahr ab heute.</span><span class="sxs-lookup"><span data-stu-id="c4d0d-137">The default end date value is one year from today.</span></span>  <span data-ttu-id="c4d0d-138">Bei einer "asymmetrischen" Art von Anmeldeinformationen muss dies auf ein oder vor dem Datum festgesetzt werden, an dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="c4d0d-138">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="c4d0d-139">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="c4d0d-139">-ObjectId</span></span>
<span data-ttu-id="c4d0d-140">Die Objekt-ID der Anwendung, der die Anmeldeinformationen hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c4d0d-140">The object id of the application to add the credentials to.</span></span>

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

### <span data-ttu-id="c4d0d-141">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="c4d0d-141">-Password</span></span>
<span data-ttu-id="c4d0d-142">Das Kennwort, das der Anwendung zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4d0d-142">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="c4d0d-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="c4d0d-143">-StartDate</span></span>
<span data-ttu-id="c4d0d-144">Der effektive Anfangstermin der Anmelde Informationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="c4d0d-144">The effective start date of the credential usage.</span></span> <span data-ttu-id="c4d0d-145">Der Standardwert für das Anfangsdatum ist heute.</span><span class="sxs-lookup"><span data-stu-id="c4d0d-145">The default start date value is today.</span></span> <span data-ttu-id="c4d0d-146">Bei einer "asymmetrischen" Art von Anmeldeinformationen muss dies auf ein oder nach dem Datum festgesetzt werden, ab dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="c4d0d-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="c4d0d-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c4d0d-147">-Confirm</span></span>
<span data-ttu-id="c4d0d-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c4d0d-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4d0d-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4d0d-149">-WhatIf</span></span>
<span data-ttu-id="c4d0d-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4d0d-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4d0d-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4d0d-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4d0d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4d0d-152">CommonParameters</span></span>
<span data-ttu-id="c4d0d-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4d0d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4d0d-154">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4d0d-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4d0d-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4d0d-155">INPUTS</span></span>

### <span data-ttu-id="c4d0d-156">System. String</span><span class="sxs-lookup"><span data-stu-id="c4d0d-156">System.String</span></span>

### <span data-ttu-id="c4d0d-157">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c4d0d-157">System.Guid</span></span>

### <span data-ttu-id="c4d0d-158">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="c4d0d-158">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="c4d0d-159">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="c4d0d-159">System.Security.SecureString</span></span>

### <span data-ttu-id="c4d0d-160">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="c4d0d-160">System.DateTime</span></span>

## <span data-ttu-id="c4d0d-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4d0d-161">OUTPUTS</span></span>

### <span data-ttu-id="c4d0d-162">Microsoft. Azure. Commands. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="c4d0d-162">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="c4d0d-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4d0d-163">NOTES</span></span>

## <span data-ttu-id="c4d0d-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4d0d-164">RELATED LINKS</span></span>

[<span data-ttu-id="c4d0d-165">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c4d0d-165">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="c4d0d-166">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c4d0d-166">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="c4d0d-167">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c4d0d-167">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

